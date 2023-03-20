<script>
import axios from "axios";
export default {
  name: "ContactsPage",
  methods: {
    sendForm() {
      console.log("ok");
    },
  },
};
</script>

<template>
  <div class="container my-5">
    <h1>Contattaci</h1>
    <form
      method="post"
      enctype="multipart/form-data"
      class="row"
      @submit.prevent="sendForm">
      <div class="col-5">
        <div class="mb-3">
          <label for="title" class="form-label">Titolo</label>
          <input type="text" class="form-control" id="title" />
        </div>
      </div>

      <div class="col-4">
        <div class="mb-3">
          <label for="email" class="form-label">Email</label>
          <input
            type="email"
            class="form-control"
            id="email"
            placeholder="name@example.com" />
        </div>
      </div>
      <div class="col-3 d-flex align-items-end justify-content-end">
        <div class="form-check form-switch mb-3">
          <input
            class="form-check-input"
            type="checkbox"
            role="switch"
            id="subscribe" />
          <label class="form-check-label" for="subscribe"
            >Iscriviti alla newsletter</label
          >
        </div>
      </div>
      <div class="col-12">
        <div class="mb-3">
          <label for="description" class="form-label">Decrizione</label>
          <textarea class="form-control" id="description" rows="3"></textarea>
        </div>
      </div>
      <div class="d-flex justify-content-end mt-4">
        <button class="btn btn-success">Invia</button>
      </div>
    </form>
  </div>
</template>

<style></style>

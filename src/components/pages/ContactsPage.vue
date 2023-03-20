<script>
import axios from "axios";
export default {
  name: "ContactsPage",
};
</script>

<template>
  <div class="container text-center my-5">
    <h1>Contattaci</h1>
    <form action="">
      <div class="col-6">
        <div class="mb-3">
          <label for="email" class="form-label">Email</label>
          <input
            type="email"
            class="form-control"
            id="email"
            placeholder="name@example.com" />
        </div>
      </div>
    </form>
  </div>
</template>

<style></style>

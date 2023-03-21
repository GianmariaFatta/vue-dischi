<script>
import axios from 'axios'
const api = 'http://127.0.0.1:8000/api/index';
export default {
    name: 'VideoGamesPage',
    data: () => ({
        videogames: null
    }),
    methods: {
        fetchVideogames() {
            axios.get(api).then(res => this.videogames = res.data.game)
        }
    },
    created() {
        this.fetchVideogames();
    }
};
</script>

<template>
    <div class="container text-center my-5">
        <h1>VIDEOGAMES</h1>
        <div class="row">
            <div v-for='videogame in videogames' :key="videogame.title" class="col-4">
                <div class="card my-3 ">
                    <div class="card-header">
                        <h4>{{ videogame.title }}</h4>
                        <div>

                            <img class='w-25' :src=videogame.image alt="">
                        </div>
                    </div>
                    <div class="card-body d-flex align-items-center">
                        <p>{{ videogame.description }}</p>
                    </div>
                    <div class="card-footer d-flex justify-content-between align-itmes-center">
                        <p>€{{ videogame.price }}</p>
                        <router-link class="btn btn-sm btn-success"
                            :to="{ name: 'videogame-details', params: { id: videogame.id } }">Vedi</router-link>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.card-header {}

.card {
    height: 380px
}
</style>
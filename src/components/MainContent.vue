<template>
    <main>
        <div class="container">
            <div class="row justify-content-center">
                <div class="col-2 gy-4 px-3" v-for="(song, index) in songList" :key="index">
                    <SongCard :song="song"/>
                </div>
            </div>
        </div>
    </main>
</template>

<script>
import axios from "axios"

import SongCard from "./SongCard.vue"
export default {
    name: "MainContent",
    components: {
        SongCard
    },
    data(){
        return{
            songList: null,
        }
    },
    created(){
         axios
        .get("https://flynn.boolean.careers/exercises/api/array/music")
        .then((res) => {
            const response = res.data.response;
            this.songList = response;
        });
    }
}
</script>

<style>
main{
    height: calc(100vh - 100px);
    background-color: #1E2D3B;
    padding-top: 50px;
    overflow-x: hidden;
}
</style>
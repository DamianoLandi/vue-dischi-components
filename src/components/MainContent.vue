<template>
    <SongCard/>
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

</style>
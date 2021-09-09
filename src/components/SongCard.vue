<template>
    <div class="song-card d-flex flex-column align-items-center justify-content-around">
        <img class="poster" :src="song.poster" alt="Poster">
        <h2 class="text-white text-center text-uppercase">{{song.title}}</h2>
        <p class="text-center">
            {{song.author}} <br> {{song.year}}
        </p>
    </div>
</template>

<script>
export default {
    name: "SongCard",
    props: ["song",]
}
</script>

<style lang="scss">
.song-card{
    background-color: #2E3A46;
    height: 350px;
    .poster{
        height: 140px;
        width: 140px;
    }

    h2{
        font-size: 25px;
    }

    p{
        color: gray;
        font-size: 18px;
    }
}

</style>
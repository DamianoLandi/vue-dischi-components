<template>
    <header>
        <img src="../assets/img/logo.png" alt="LOGO" id="logo">
    </header>
</template>

<script>
export default {
    name: "Header"
}
</script>

<style scoped lang="scss">
    header{
        height: 100px;
        background-color: #2E3A46;
        #logo{
            height: 80px;
            margin-top: 10px;
            margin-left: 10px;
        }
    }
</style>
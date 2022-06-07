<template>
    <main>
      <img src="../../assets/img/spotify-logo.png" alt="logo-spotify">  
    </main>
</template>

<script>
export default {
    name: 'BaseHeader',
}
</script>

<style lang="scss" scoped>
main {
    background-color: #2e3a46;

    & img {
        max-width: 4%;
        padding: 10px;
    }
}
</style>
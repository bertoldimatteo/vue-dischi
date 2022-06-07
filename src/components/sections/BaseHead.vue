<template>
    <header>
      <img src="../../assets/img/spotify-logo.png" alt="logo-spotify">  
    </header>
</template>

<script>
export default {
    name: 'BaseHeader',
}
</script>

<style lang="scss" scoped>
header {
    background-color: var( --primary-color);
    max-height: 66px;

    & img {
        max-width: 4%;
        padding: 10px;
    }
}
</style>
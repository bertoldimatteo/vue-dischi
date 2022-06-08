<template>
    <header>
        <div class="header-container">
            <div class="image">
                <img src="../../assets/img/spotify-logo.png" alt="logo-spotify"> 
            </div> 
        </div>
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
    height: 66px;
    max-height: 66px;

    & img {
        max-width: 9%;
        padding: 10px;
    }
}
.header-container {
    display: flex;
    align-items: center;
    justify-content: space-between;
}
</style>
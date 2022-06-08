<template>
    <header>
        <div class="header-container">
            <div class="image">
                <img src="../../assets/img/spotify-logo.png" alt="logo-spotify"> 
            </div> 
            <SelectBar/>
        </div>
    </header>
</template>

<script>
import SelectBar from '../commons/SelectBar.vue'
export default {
    name: 'BaseHeader',
    components: { 
        SelectBar 
    },
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
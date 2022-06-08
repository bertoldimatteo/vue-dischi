<template>
    <header>
        <div class="header-container">
            <div class="image">
                <img src="../../assets/img/spotify-logo.png" alt="logo-spotify"> 
            </div> 
            <div class="select-form">
                <label for="music">Genere:</label>
                <select id="genere" name="genre-music" form="musicGenre">
                    <option value="Rock">Rock</option>
                    <option value="Pop">Pop</option>
                    <option value="Jazz">Jazz</option>
                    <option value="Metal">Metal</option>
                </select>
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
.select-form {
    color: #fff;
}
select {
    margin: 10px;
}
</style>
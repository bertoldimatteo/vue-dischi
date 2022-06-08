<template>
    <div class="select-form">
        <label for="music">Genere:</label>
        <select id="genere" name="genre-music" form="musicGenre">
            <option value="All">All</option>
            <option value="Rock">Rock</option>
            <option value="Pop">Pop</option>
            <option value="Jazz">Jazz</option>
            <option value="Metal">Metal</option>
        </select>
    </div>
</template>

<script>
export default {
    name: 'SelectBar',
}
</script>

<style lang="scss" scoped>
.select-form {
    color: #fff;
}
select {
    margin: 10px;
}
</style>
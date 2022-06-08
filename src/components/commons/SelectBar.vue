<template>
    <div class="select-form">
        <label>Genere:</label>
        <select v-model="selectFilter" @click.capture="$emit('searching', selectFilter)">
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
    data() {
        return {
            selectFilter: '',
        }
    }
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
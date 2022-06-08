<template>
    <div class="select-form">
        <label>Genere:</label>
        <select v-model="dataShared.selectFilter" @change="$emit('searching', selectFilter)">
            <option value="All">All</option>
            <option value="Rock">Rock</option>
            <option value="Pop">Pop</option>
            <option value="Jazz">Jazz</option>
            <option value="Metal">Metal</option>
        </select>
    </div>
</template>

<script>
import dataShared from '../../shared/dataShared.js'

export default {
    name: 'SelectBar',
    data() {
        return {
            dataShared
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
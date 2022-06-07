<template>
  <main>
    <div class="container">
        <div class="row">
            <MusicCard class="col" v-for="(music ,index) in musics" :key="index" :music="music"/>      
        </div>
    </div>
  </main>
</template>

<script>
import axios from 'axios';
import MusicCard from '../commons/MusicCard.vue';

export default {
    name: 'BaseMain',
    data() {
        return {
            musics: [],
        }
    },
    components: {
        MusicCard,
    },
    created() {
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then((response) => {
            // handle success
            this.musics = response.data.response;
        })
        .catch((error) => {
            // handle error
            console.log(error);
        })
    }
}
</script>

<style lang="scss" scoped>
main {
    background-color: var(--seconday-color);
}
.row {
    max-width: 1220px;
    margin: auto;
    display: flex;
    flex-wrap: wrap;
    
}
.col {
    width: calc(100% / 5 - 30px);
    margin: 15px;
}
</style>
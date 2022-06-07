<template>
  <main>
    <div class="container">
        <div class="row">
            <MusicCard class="col-sm-12 col-md-4 col-lg" v-for="(music ,index) in musics" :key="index"/>      
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
.container {
    padding: 100px;
}
</style>
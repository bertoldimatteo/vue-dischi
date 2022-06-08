<template>
  <main>
    <div class="container">
        <div class="row">
            <MusicCard class="col" v-for="(music ,index) in musicFiltered" :key="index" :music="music"/>      
        </div>
        <div class=selectBar>
            <SelectBar @searching="filterMusic"/>
        </div>
    </div>
  </main>
</template>

<script>
import axios from 'axios';
import MusicCard from '../commons/MusicCard.vue';
import SelectBar from '../commons/SelectBar.vue'

export default {
    name: 'BaseMain',
    data() {
        return {
            musics: [],
            payload: '',
        }
    },
    components: {
        MusicCard,
        SelectBar, 
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
    },
    methods: {
        filterMusic(payload) {
            this.payload = payload;
        }
    },
    computed: {
        musicFiltered() {
            return this.musics.filter((elm) => elm.genre.includes(this.payload));
        }
    },
}
</script>

<style lang="scss" scoped>
main {
    background-color: var(--seconday-color);
    height: calc(100vh - 66px)
}
.container {
    display: flex;
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
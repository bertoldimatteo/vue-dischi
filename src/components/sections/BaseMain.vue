<template>
  <main>
    <div class="container">
        <div class="row">
            <div class="col-12 col-sm-6 col-md-4 col-lg-3 music-card"></div>
        </div>
    </div>
  </main>
</template>

<script>
import axios from 'axios';
export default {
    name: 'BaseMain',
    data() {
        return {
            musics: [],
        }
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
.music-card {
    background-color: var(--primary-color);
}
</style>
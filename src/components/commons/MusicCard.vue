<template>
  <div class="card">
      <img :src="music.poster" alt="music.author">
      <h2>{{music.title}}</h2>
      <p>{{music.author}}</p>
      <span>{{music.year}}</span>
  </div>
</template>

<script>
export default {
    name: 'MusicCard',
    props: {
        music: Object,
    }
}
</script>

<style lang="scss" scoped>
.card {
    background-color: var(--primary-color);
    max-height: 380px;
    height: 380px;
    padding: 20px;
    text-align: center;
    
    & h2 {
        color: #fff;
        margin-top: 10px;
        font-size: 29px;
    }

    & img {
        width: 100%;
    }

    & p {
        margin-top: 20px;
        margin-bottom: 0.5px; 
    }
    & p, span {
        color: #808080;
    }
    & span {
        font-size: 13px;
    }
}
</style>
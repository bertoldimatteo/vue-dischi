<template>
  <div class="card">
      <img src="http://www.asdalcione.it/wp-content/uploads/2016/08/jk-placeholder-image-1.jpg" alt="placeholder">
      <h2>Titolo album</h2>
      <p>Autore Album</p>
      <span>Anno album</span>
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
    max-width: 230px;
    width: 230px;
    max-height: 350px;
    height: 350px;
    padding: 20px;
    text-align: center;
    
    & h2 {
        color: #fff;
        margin-top: 15px;
    }

    & p {
        margin-top: 20px;
        margin-bottom: 0.5px; 
    }
    & p, span {
        color: #808080;
    }
}
</style>
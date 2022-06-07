<template>
  <div class="album">
      <img :src="album.poster" :alt="album.author">
      <h4 class="my-3">{{album.title}}</h4>
      <h5>{{album.author}}<br>{{album.year}}</h5>
  </div>
</template>

<script>
export default {
    name: 'AlbumComponent',
    props: {
        album: Object,
    }
}
</script>

<style lang="scss" scoped>
    .album {
        background-color: var(--primary_bg_color);
        text-align: center;
        padding: 1.25rem;
        img {
            width: 100%;
        }
    }

</style>
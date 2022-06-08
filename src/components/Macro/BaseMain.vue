<template>
  <main>
      <AlbumSection/>
  </main>
</template>

<script>
import AlbumSection from '../Sections/AlbumSection.vue';
export default {
    name: "BaseMain",
    components: { 
        AlbumSection 
    }
}
</script>

<style lang="scss" scoped>
    
    main {
        background-color: var(--main_bg_color);
        min-height: 62.5rem;
    }
</style>
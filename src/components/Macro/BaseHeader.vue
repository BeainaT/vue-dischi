<template>
  <header>
      <div class="container-fluid py-2">
        <HeaderLogo/>
      </div>
  </header>
</template>

<script>
import HeaderLogo from '../Commons/HeaderLogo.vue';

export default {
    name: "BaseHeader",
    components: { 
        HeaderLogo 
    }
}
</script>

<style lang="scss" scoped>
    header {
        background-color: var(--primary_bg_color);
    }
</style>
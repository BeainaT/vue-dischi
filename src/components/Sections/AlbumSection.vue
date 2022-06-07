<template>
  <section>
      <LoaderSpin/>
      <div class="container py-5 v-else">
          <div class="row gap-4 justify-content-center">
              <AlbumComponent class="col-sm-12 col-md-4 col-xl-2" v-for="(album, index) in albums" :key="index" :album="album"/>
          </div>
      </div>
  </section>
</template>

<script>
import axios from 'axios';
import AlbumComponent from '../Commons/AlbumComponent.vue';
import LoaderSpin from '../Commons/LoaderSpin.vue';


export default {
    name: 'AlbumSection',
    components: {
        AlbumComponent,
        LoaderSpin
    },
    data() {
        return {
            albums: [],
            loading: true,
        }
    },
    created() {
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then((response) => {
            this.albums = response.data.response;
            this.loading = false;
        })
        .catch((error) => {
            console.log(error);
        });
    }
    
}
</script>

<style>

</style>
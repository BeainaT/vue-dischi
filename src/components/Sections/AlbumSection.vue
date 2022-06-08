<template>
  <section>
      <LoaderSpin v-if="loading" />
      <div class="container py-5 v-else">
          <MainSelect @search="filterGenre"/>
          <div class="row gap-4 justify-content-center">
              <AlbumComponent class="col-sm-12 col-md-4 col-xl-2" v-for="(album, index) in filteredAlbum" :key="index" :album="album"/>
          </div>
      </div>
  </section>
</template>

<script>
import axios from 'axios';
import AlbumComponent from '../Commons/AlbumComponent.vue';
import LoaderSpin from '../Commons/LoaderSpin.vue';
import MainSelect from '../Commons/MainSelect.vue';

export default {
    name: 'AlbumSection',
    components: {
    AlbumComponent,
    LoaderSpin,
    MainSelect
},
    data() {
        return {
            albums: [],
            loading: true,
            filteredAlbum: [],
        }
    },
    created() {
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then((response) => {
            this.albums = response.data.response;
            this.filteredAlbum = response.data.response;
            this.loading = false;
        })
        .catch((error) => {
            console.log(error);
        });
    },
    methods: {
        filterGenre(selectedGenre) {
            this.filteredAlbum = this.albums.filter((album) => album.genre == selectedGenre);
            if(selectedGenre == 'all') {
                this.filteredAlbum = this.albums;
            }
            console.log(selectedGenre)
        }
    }
    // computed: {
    //     filteredAlbum() {
    //         return this.albums;
    //     }
    // }
    
}
</script>

<style>

</style>
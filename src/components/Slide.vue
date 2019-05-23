
<template>
    <img v-if="loading" src="https://i.imgur.com/JfPpwOA.gif">
    <ul v-else>
         <carousel :autoplay="true" :nav = "false" :margin="20" :responsive="{300:{items:2},600:{items:1,}}">
            <li v-for="img in imgs">
                <img class="img-owl" v-bind:src="img.urls.raw" />
            </li>
        </carousel>
    </ul>
</template>

<script>
import axios from 'axios';
import carousel from 'vue-owl-carousel'

 export default {  
    components: {
        carousel
    },
    data () {
      return {
        loading: false,
        imgs: [],
        errors:[]
      }
    },

     created () {
      this.loading = true
      axios.get(`https://api.unsplash.com/search/photos?query=wunderlust&client_id=17d5a1a913147195c8fce4e1c40d29c029a126dba1d5e1f3e1ce72aa8df09bff`)
      .then(response => {
      // JSON responses are automatically parsed.
      this.imgs = response.data.results
      })
      .catch(e => {
      this.errors.push(e)
      })
    .then(
        () => this.loading = false
      )
    }
 }
</script>

<style scoped>
    ul li {
        list-style: none;
    }
    .img-owl{
        max-height:500px;
    }
</style>

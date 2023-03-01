<script setup>
import { onMounted, ref} from 'vue';

import Magnify from "vue-material-design-icons/Magnify.vue"
import HomeOutline from "vue-material-design-icons/HomeOutline.vue"
import TrendingUp from "vue-material-design-icons/TrendingUp.vue"
import Television from "vue-material-design-icons/Television.vue"
import MovieOutline from "vue-material-design-icons/MovieOutline.vue"
import Plus from "vue-material-design-icons/Plus.vue"
import ChevronLeft from "vue-material-design-icons/ChevronLeft.vue"

import {useMovieStore} from './stores/movie'
import {storeToRefs} from 'pinia'

const useMovie = useMovieStore();
const {movie , showFullVideo} = storeToRefs(useMovie);


</script>

<template>
  <div class="fixed w-full h-screen bg-black">
      <div v-if="!showFullVideo" id="SideNav" class="flex z-40 items-center w-[120px] h-screen bg-black relative ">
          image
          <div>
              <div class="py-2 mx-10 my-6">
                  <Magnify fillColor="#fff" :size="40" class=""/>
              </div>
              <div class="py-2 mx-10 my-6 border-red-600 border-b-4">
                  <HomeOutline fillColor="#fff" :size="40" class=""/>
              </div>
              <div class="py-2 mx-10 my-6">
                  <TrendingUp fillColor="#fff" :size="40" class=""/>
              </div>
              <div class="py-2 mx-10 my-6">
                  <Television fillColor="#fff" :size="40" class=""/>
              </div>
              <div class="py-2 mx-10 my-6">
                  <MovieOutline fillColor="#fff" :size="40" class=""/>
              </div>
              <!-- https://youtu.be/PYz021FzZhg?t=546 -->
              <div class="py-2 mx-10 my-6">
                  <Plus fillColor="#fff" :size="40" class=""/>
              </div>
              <div class="py-2 mx-10 my-6">
                  <ChevronLeft fillColor="#fff" :size="40" class=""/>
              </div>
          </div> 
      </div>
  </div>
</template>

<style scoped>

</style>

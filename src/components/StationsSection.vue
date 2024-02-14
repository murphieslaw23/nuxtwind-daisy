<template>
  <div class="container">
    <div class="hero min-h-screen bg-base-100" v-for="nowplaying in nowPlayingArray" v-bind:key="nowplaying" >
        <div class="hero-content flex-col lg:flex-row">
          <img :src="nowplaying.now_playing.song.art" class="w-50 rounded-lg shadow-2xl" />
          <div>
            <h1 class="text-5xl font-bold">{{nowplaying.station.name}}</h1>
            <p class="py-6">{{nowplaying.station.description}}</p>
            <NuxtLink :to="'station/'+ nowplaying.station.shortcode "><button class="btn btn-primary">Listen Now!</button></NuxtLink>
          </div>
        </div>
      </div>
  </div>

</template>

<script lang="ts" setup>
const { data: nowPlayingArray } = await useFetch('https://www.subculturesound.de/api/nowplaying');
</script>

<style>

</style>

<template>
  <div class="container text-center sm:text-left mb-3">
    <h1>{{ station.name }}</h1>
  </div>
</template>

<script>
import { defineComponent } from '@vue/composition-api';
import { useRoute } from 'vue-router';

export default defineComponent({

  async setup () {
    const route = useRoute();
    const { data: station } = await useFetch('https://www.subculturesound.de/api/station/' + route.params.shortcode);

    return {
      station,
    };
  },
});
</script>

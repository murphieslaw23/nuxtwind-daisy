<template>
  <div class="container text-sm text-center sm:text-left mb-3 ">
    <div><h1>WELCOME</h1></div>
    <div>
      <StationsSection />
    </div>
  </div>
</template>

<script>
import { useHead } from '#app';
import { definePageMeta } from '#imports';
import ogBanner from '../assets/images/subculturesound-logo.png';

export default {
  setup () {
    definePageMeta({
      layout: 'default',
    });

    useHead({
      title: 'SUBCULTURESOUND - RARE ELECTRONIC MIXES',
      description: 'Description Text',
      link: [
        { rel: 'icon', type: 'image/png', href: '/favicon.png' },
      ],
      meta: [
        {
          hid: 'og:image',
          name: 'og:image',
          property: 'og:image',
          content: ogBanner,
        },
      ],
    });

    return {};
  },
};
</script>

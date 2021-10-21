<template>
  <v-app>
    <v-main>
     <multiple-counters />
    </v-main>
  </v-app>
</template>

<script>

import MultipleCounters from './components/MultipleCounters.vue';

export default {
  name: 'App',

  components: {
    MultipleCounters,
  },

  data: () => ({
  }),
};
</script>

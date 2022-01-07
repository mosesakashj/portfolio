<template>
  <v-app>
    <v-main>
      <HelloWorld/>
    </v-main>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';

export default {
  name: 'App',

  components: {
    HelloWorld,
  },

  data: () => ({
    //
  }),
};
</script>
<style>
html {
  -ms-overflow-style: none !important;
  scrollbar-width: none !important;
  user-select: none !important;
}
html::-webkit-scrollbar {
  display: none;
}
</style>

<template>
  <v-app>
    <app-system-bar> </app-system-bar>
    <app-bar></app-bar>
    <app-main-index></app-main-index>
    <app-footer></app-footer>
  </v-app>
</template>

<script>
import appSystemBar from './components/app-system-bar';
import appBar from './components/app-bar';
import appFooter from './components/app-footer';
import appIndexMain from './components/index/app-index-main';
export default {
  name: 'Index',

  components: {
    "app-system-bar": appSystemBar,
    "app-bar": appBar,
    "app-main-index": appIndexMain,
    "app-footer": appFooter, 
  },

  data: () => ({
    //
  }),
};
</script>

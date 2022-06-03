<template>
    <v-app>
        <app-system-bar> </app-system-bar>
        <app-bar></app-bar>
        <app-about-main></app-about-main>
        <app-footer></app-footer>
    </v-app>
</template>
<script>
import appSystemBar from './components/app-system-bar';
import appBar from './components/app-bar';
import appFooter from './components/app-footer';
import appAboutMain from './components/about/app-about-main';
export default {
  name: 'About',

  components: {
    "app-system-bar": appSystemBar,
    "app-bar": appBar,
    "app-footer": appFooter, 
    "app-about-main": appAboutMain
  },

  data: () => ({
    //
  }),
};
</script>
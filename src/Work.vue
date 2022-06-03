<template>
    <v-app>
        <app-system-bar> </app-system-bar>
        <app-bar></app-bar>
        <app-work-main></app-work-main>
        <app-footer></app-footer>
    </v-app>
</template>
<script>
import appSystemBar from './components/app-system-bar';
import appBar from './components/app-bar';
import appFooter from './components/app-footer';
import appWorkMain from './components/work/app-work-main';
export default {
  name: 'Index',

  components: {
    "app-system-bar": appSystemBar,
    "app-bar": appBar,
    "app-footer": appFooter, 
    "app-work-main": appWorkMain
  },

  data: () => ({
    //
  }),
};
</script>
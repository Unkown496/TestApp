<template>
    <v-app>
        <app-system-bar> </app-system-bar>
        <app-bar></app-bar>
        <app-company-main></app-company-main>
        <app-footer></app-footer>
    </v-app>
</template>
<script>
import appSystemBar from './components/app-system-bar';
import appBar from './components/app-bar';
import appFooter from './components/app-footer';
import appCompanyMain from './components/company/app-company-main';
export default {
  name: 'Company',

  components: {
    "app-system-bar": appSystemBar,
    "app-bar": appBar,
    "app-footer": appFooter, 
    "app-company-main": appCompanyMain
  },

  data: () => ({
    //
  }),
};
</script>

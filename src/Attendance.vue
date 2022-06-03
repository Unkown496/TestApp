<template>
    <v-app>
      <app-system-bar> </app-system-bar>
      <app-bar></app-bar>
      <app-main-att></app-main-att>
      <app-footer></app-footer>
    </v-app>
  </template>
  
  <script>
  import appSystemBar from './components/app-system-bar';
  import appBar from './components/app-bar';
  import appFooter from './components/app-footer';
  import appAttMain from './components/attendance/app-attendance-main';
  export default {
    name: 'Attendance',
  
    components: {
      "app-system-bar": appSystemBar,
      "app-bar": appBar,
      "app-main-att": appAttMain,
      "app-footer": appFooter, 
    },
  
    data: () => ({
      //
    }),
  };
  </script>
  
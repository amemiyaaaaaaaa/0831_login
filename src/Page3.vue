<template>
  <v-ons-page>
    <custom-toolbar :back-label="'Page 3'">ログイン成功</custom-toolbar>
    <p style="text-align: center">ログイン成功</p>
     <v-ons-button @click="push">ログイン</v-ons-button>
  </v-ons-page>
</template>

<script>
  import customToolbar from './CustomToolbar';
  import app from './App';
  import page1 from './Page1';

  export default {
    methods: {
      pop() {
        this.pageStack.pop();
      } ,
      push() {
         this.pageStack.push(page1);
       }
    },
    props: ['pageStack'],
    components: { customToolbar },
    key: 'key_page3',
  }
</script>

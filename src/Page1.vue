<template id="signup">
  <v-ons-page>

    <custom-toolbar>ログイン</custom-toolbar>
    <p style="text-align: center">
        <p>キャッチコピーららららら</p> 
  <h1>おたカレ</h1>
    <form method="post" action="">
     <p>ユーザー名： <input type="text" name="name"></p>
     <p>パスワード： <input type="password" name="pass"></p>
    </form>
      <v-ons-button @click="push">新規登録</v-ons-button>
      <v-ons-button @click="push">ログイン</v-ons-button>
      
    </p>
  </v-ons-page>
</template> 

<script>
  import customToolbar from './CustomToolbar';
  import page2 from './Page2';

  export default {
  
     methods: {
       pop(){
         this.pageStack.pop();
       },
       push() {
         this.pageStack.push(page2);
       },
       
     },
     props: ['pageStack'],
     components: { customToolbar },
     key: 'key_page1',
  }
</script>

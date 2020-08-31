<template>
  <v-ons-page>
    <custom-toolbar>新規登録</custom-toolbar>
    <p style="text-align: center">
     <div class=""> 
       <h1>新規登録</h1>
       <h2>入力画面</h2>
           <form method="post" action="">
            <p>ユーザー名： <input type="text" name="name"></p>
            <p>パスワード： <input type="password" name="pass"></p>
        </form>
        <h2>アプリ利用規約</h2>
            <p> 利用規約～～ </p> 
            <input type="checkbox" id="checkbox" v-model="checked">
             <label for="checkbox">{{ checked }}利用規約に同意します</label>
     </div>
    </form>  
      <v-ons-button @click="push">確定</v-ons-button>
    </p>
  </v-ons-page>
</template>

<script>
  import customToolbar from './CustomToolbar';
  import page3 from './Page3';
  export default {
     methods: {
       pop(){
         this.pageStack.pop();
       },
       push() {
         this.pageStack.push(page3);
       }
     },
     props: ['pageStack'],
     components: { customToolbar },
     key: 'key_page2',
  }
</script>

<template>
  <div id="app">
    <h1>Молочный бар Korova</h1>
    <hr>
    <!-- Фрагмент для регистрации, по умолчанию он включен.
    При прохождении пользователем регистрации флаг заменяется
    на true и фрагмент отключается и заместо него будет виден Logout.
     Я начинаю реализацию кода с этого фрагмента, поэтому в нем код, где
     есть ошибка с получением JSON-файла-->
    <HeadReg
            v-if="REG_FLAG === false"
            v-on:loginTo="loginTo"
    />
    <Logout v-else />
    <hr>
    <!-- Всплывающее окно регистрации -->
    <WindowReg
            v-if="WinReg_FLAG"
    />
    <!-- Всплывающее окно редактирования постов -->
    <WindowEdit
            v-if="EDIT_FLAG"
    />
    <ListBlog
            v-bind:REG_FLAG="REG_FLAG"
    />
  </div>
</template>

<script>

  import Logout from "@/components/Logout";
  import HeadReg from "@/components/HeadReg";
  import ListBlog from "@/components/ListBlog";
  import WindowEdit from "@/components/WindowEdit";
  import WindowReg from "@/components/WindowReg";
  export default {
    name: 'app',
    data(){
      return {
        REG_FLAG: false,
        EDIT_FLAG: false,
        WinReg_FLAG: false
      }
    },
    methods: {
      loginTo(){

      },
    },
    components: {
      HeadReg,
      ListBlog,
      Logout,
      WindowEdit,
      WindowReg,
    }
  }
</script>

<style>
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 15px;
  }
</style>

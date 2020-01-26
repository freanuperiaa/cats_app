<template>
  <div id="app">
    <b-container>
      <div class="app-header"></div>
      <app-header></app-header>
      <b-row>
        <b-col cols="7" class="column-one">1 of 2</b-col>
        <b-col cols="5" class="column-two">
          <app-cat></app-cat>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
import Header from './components/Header.vue';
import CatColumn from './components/CatColumn.vue';

export default {
  components: {
      appHeader: Header,
      appCat: CatColumn,
  },
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

</style>

<template>
  <div id="app">
    <b-container>
      <div class="app-header"></div>
      <app-header
        :isInitialized="catData.isInitialized"
      ></app-header>
      <b-row>
        <b-col cols="7" class="column-one">
          <div v-if="catData.isInitialized">
            <!-- TODO: INSERT COMPONENT HERE PLZZ -->
            <h4>since the cat has been initialized, content should be here.</h4>
          </div>
          <div v-else>
            <app-cat-start></app-cat-start>
            <!-- TODO: give property (type:function) that will initialize cat after form has been submitted.-->
          </div>
        </b-col>
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
import CatStart from './components/CatStart.vue';

export default {
  components: {
      appHeader: Header,
      appCat: CatColumn,
      appCatStart: CatStart,
  },
  data: function() {
    return {
      catData: {
        name: '',
        breed: '',
        age: 0,
        characteristics: [],
        status: {
          happiness:0,
          hunger: 0,
          entertained: 0,
        },
        isInitialized: false,
      },
      currentPage: '',
    };
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
  margin-top: 60px;
}

</style>

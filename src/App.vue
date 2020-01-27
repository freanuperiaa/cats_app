<template>
  <div id="app">
    <b-container>
      <div class="app-header"></div>
      <app-header
        :isInitialized="isInitialized"
        :currentPage="currentComponent"
        :changePage="changePage"
      ></app-header>
      <b-row>
        <b-col cols="7" class="column-one">
          <div v-if="isInitialized">
            <component :is="currentComponent">
              <p>Default Content</p>
            </component>
          </div>
          <div v-else>
            <app-cat-start
              :createCat="createCat"
            ></app-cat-start>
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
import Home from './components/Home.vue';
import Care from './components/Care.vue';
import Play from './components/Play.vue';
import MyCat from './components/MyCat.vue';

export default {
  components: {
      appHeader: Header,
      appCat: CatColumn,
      appCatStart: CatStart,
      appHome: Home,
      appCare: Care,
      appPlay: Play,
      appMyCat: MyCat,
  },
  data: function() {
    return {
      catData: {
        name: '',
        breed: '',
        age: 0,
        description:'' ,
        status: {
          happiness:0,
          hunger: 0,
          entertained: 0,
        },
      },
      isInitialized: false,
      currentComponent: Home,
    };
  },
  methods: {
    createCat(name, breed, age, description) {
      console.log('reached here!');
      this.catData.name = name;
      this.catData.breed = breed;
      this.catData.age = age;
      this.catData.description = description;
      this.catData.status['happiness'] = 100;
      this.catData.status['hunger'] = 0;
      this.catData.status['entertained'] = 100;
      this.isInitialized = true;
    },
    changePage(page) {
      this.currentComponent = page;
    },
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

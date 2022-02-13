<template>
  <div id="app">
    <father-1></father-1>
    <filters-prac></filters-prac>
    <model-prac :content="content" @input="content =$event"></model-prac>
    组件上的v-model：{{content}}
    <vue-set></vue-set>
    <direct></direct>
  </div>
</template>

<script>
import Father1 from './components/Father1.vue'
import FiltersPrac from './components/filtersPrac.vue'
import ModelPrac from './components/modelPrac.vue'
import VueSet from './components/VueSet.vue'
import Direct from './components/CustomDirectives.vue'
export default {
  name: 'App',
  components: {
    Father1,
    FiltersPrac,
    ModelPrac,
    VueSet,
    Direct
  },
  data(){
    return{
      content:'v-model内容'
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

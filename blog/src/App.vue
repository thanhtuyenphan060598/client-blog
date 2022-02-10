<template>
    <div class=" vue-tempalte" id="app" >
      <Header></Header>
      <Main></Main>
      <Footer></Footer>
      
    </div>
</template>

<script>
import Main from './components/main/Main.vue'
import Header from './components/header/Header.vue'
import Footer from './components/footer/Footer.vue'
import {mapActions} from 'vuex'



export default {
  data() {
    return {
      
    }
  },
  
  methods: {
    ...mapActions(['GetPosts'])
  },
  components :{
    Main,
    Footer,
    Header,
    
  },
   mounted() {
    this.GetPosts()
  },
 
}
</script>

<style>

</style>

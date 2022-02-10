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
import {mapGetters} from 'vuex'



export default {
  data() {
    return {
      
    }
  },
  computed : {
    ...mapGetters(['StateUser']),
  },
  components :{
    Main,
    Footer,
    Header,
    
  },
  watch : {
    StateUser() {
      this.$router.push('/newest')
    }
  }
}
</script>

<style>

</style>

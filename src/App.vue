<script>
import AppHeader from './components/AppHeader.vue';
import AppFooter from './components/AppFooter.vue';
import AppMain from './components/AppMain.vue';
import Loading from './components/loading.vue'
export default {
  components:{
    AppHeader,
    AppMain,
    AppFooter,
    Loading
  },
  data(){
    return{
      loading: false,
      nav:[
        'Home',
        'About Us',
        'Portfolio', 
        'Our Process', 
        'Pricing', 
        'Blog', 
        'Contact',
        'Get a Quote'
      ],
      secondNav:[
        'About Us',
        'Portfolio', 
        'Pricing', 
        'Career', 
        'Contact',
      ]
    }
  },
  mounted(){
    this.loadActive()
  },
  methods:{
    loadActive(){
      setInterval(() => {
        this.loading = true
      }, 2000);
    }
  }
}
</script>
<template lang="">
  <div v-if="!loading">
    <Loading/>
  </div>
  <div v-else>
    <AppHeader :navbar="nav"/>
    <AppMain/> 
    <AppFooter :navbar="secondNav"/>
  </div>
</template>
<style lang="scss">
  @use './styles/generals.scss';
</style>
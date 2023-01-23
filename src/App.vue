<script>
import AppHeader from './components/AppHeader.vue';
import AppFooter from './components/AppFooter.vue';
import AppMain from './components/AppMain.vue'
export default {
  components:{
    AppHeader,
    AppMain,
    AppFooter
  },
  data(){
    return{
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
  }
}
</script>
<template lang="">
  <div>
    <AppHeader :navbar="nav"/>
    <AppMain/> 
    <AppFooter :navbar="secondNav"/>
  </div>
</template>
<style lang="scss">
  @use './styles/generals.scss';
</style>
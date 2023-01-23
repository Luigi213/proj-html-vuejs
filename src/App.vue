<script>
import AppHeader from './components/AppHeader.vue';
import AppFooter from './components/AppFooter.vue';
export default {
  components:{
    AppHeader,
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
    <AppFooter :navbar="secondNav"/>
  </div>
</template>
<style lang="scss">
  @use './styles/generals.scss';
</style>
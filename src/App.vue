<template>
  <div id="app">
    <component :is="layout">
      <router-view/>
    </component>
  </div>
</template>

<script>
import DarckLayout from '@/layouts/DarckLayout'
import MainLayout from '@/layouts/MainLayout'
export default {
  computed:{
    layout(){
      return (this.$route.meta.layout || 'darck') + '-layout'
    }
  },
  components:{
    DarckLayout, MainLayout
  }
}
</script>


<style lang="scss">
@import '~materialize-css/dist/css/materialize.min.css';
@import 'assets/index.css';

</style>

<template>
<v-app class="gray lighten-4">
  <!--<Navbar/> -->
  <Appbar/>
  <v-content>
    <router-view></router-view>
  </v-content>
 
 </v-app>
</template>

<script>
//import Navbar from '@/components/Navbar'
import Appbar from '@/components/Appbar'
export default {
  name: 'App',
  components: {Appbar},
  data(){
    return{
      //
    }
  }
}
</script>

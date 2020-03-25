<template>
    <nav>
     
            <v-toolbar prominent extended color="green">
                <v-app-bar-nav-icon></v-app-bar-nav-icon>
                <v-toolbar-title class="text-uppercase">
                <span class="font-weight-light">Todo</span>
                <span>Ninja</span>
                </v-toolbar-title>
                <v-spacer></v-spacer>
                <v-btn flat color="red lighten-2">
                <span>Sign out</span>
                <v-icon right>{{svgPath}}</v-icon>
                </v-btn>
            </v-toolbar>
            
     
     
    </nav>
  
</template>

<script>
import {mdiArrowRightBox} from '@mdi/js'
export default {
    data:() =>({
        svgPath: mdiArrowRightBox
    
    }),
}
</script>
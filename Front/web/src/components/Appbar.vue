<template>
    <nav>
      <v-app-bar app color="white" height="100" class="primary">
      <v-img
          contain
          max-width="60px"
          max-height="70%"
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-logo-dark.png"
        ></v-img>
     
      <v-toolbar-title class="font-weight-black headline" pa-3>
        VUE BOURSE
      </v-toolbar-title>
        
      <v-container mx-auto py-2>
        <v-layout>
          <v-btn 
          v-for="(link,i) in links"
          :key="i"
          :to="link.to"
          class="ml-0 hidden-sm-and-down"
          flat
          @click="OnClick($event,item)">

            {{link.text}}
          </v-btn>
          <v-spacer />
          <v-text-field
          append-icon="mdi-magnify"
          flat 
          hide-details
          solo-inverted
          style="max-width: 300px;"/>
        </v-layout>
      </v-container>
        
     
    </v-app-bar>
   
    </nav>
   
</template>

<script>
// Utilities
import {
  mapGetters,
  mapMutations
} from 'vuex'

export default {
      computed: {
      ...mapGetters(['links'])
    },

    methods: {
      ...mapMutations(['toggleDrawer']),
      onClick (e, item) {
        e.stopPropagation()

        if (item.to || !item.href) return

        this.$vuetify.goTo(item.href)
      }
    }
}
</script>
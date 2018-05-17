<template>
    <v-app>
            <v-navigation-drawer
            :clipped="$vuetify.breakpoint.lgAndUp"
            v-model="drawer"
            fixed
            app
            >
            <v-list dense>
                <template v-for="item in items">
                <v-layout
                    v-if="item.heading"
                    :key="item.heading"
                    row
                    align-center
                >
                    <v-flex xs6>
                    <v-subheader v-if="item.heading">
                        {{ item.heading }}
                    </v-subheader>
                    </v-flex>
                    <v-flex xs6 class="text-xs-center">
                    <a href="#!" class="body-2 black--text">EDIT</a>
                    </v-flex>
                </v-layout>
                <v-list-tile v-else :key="item.text" @click="">
                    <v-list-tile-action>
                    <v-icon>{{ item.icon }}</v-icon>
                    </v-list-tile-action>
                    <v-list-tile-content>
                    <v-list-tile-title>
                        {{ item.text }}
                    </v-list-tile-title>
                    </v-list-tile-content>
                </v-list-tile>
                </template>
            </v-list>
            </v-navigation-drawer>
        
        <v-toolbar 
        :clipped-left="$vuetify.breakpoint.lgAndUp"
        app
        fixed
        color="white">
            <v-toolbar-side-icon @click.stop="drawer = !drawer"></v-toolbar-side-icon>
            <v-toolbar-title>Dive Your Choice</v-toolbar-title>
            <v-spacer></v-spacer>

            <div>
                <v-toolbar-items class="hidden-sm-and-down">
                    <router-link to="/" tag="span">
                        <v-btn icon>
                            <v-icon>home</v-icon>
                        </v-btn>
                    </router-link>
                    <router-link to="/Login" tag="span">
                        <v-btn flat>Log In</v-btn>
                    </router-link>   
                    <v-btn flat>Help</v-btn>
                </v-toolbar-items>
            </div>
        </v-toolbar>
    </v-app>
</template>

<script>
  export default {
    data: () => ({
      dialog: false,
      drawer: null,
      items: [
        { icon: 'assignment', text: 'Manifest', link:'/'},
        { icon: 'payment', text: 'Bills', link: '/Billing' },
        { icon: 'shopping_cart', text: 'Products' },
      ]
    }),
    props: {
      source: String
    }
  }
</script>

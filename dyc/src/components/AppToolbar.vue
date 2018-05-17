<template>
    <v-toolbar color="white">
        <v-toolbar-side-icon @click.native.stop="mini = !mini"></v-toolbar-side-icon>
        <v-toolbar-title>Dive Your Choice</v-toolbar-title>
        <v-spacer></v-spacer>

        <div>
            <v-toolbar-items class="hidden-sm-and-down">
                <router-link to="/">
                    <v-btn icon>
                        <v-icon>home</v-icon>
                    </v-btn>
                </router-link>
                <router-link to="/Login">
                    <v-btn flat>Log In</v-btn>
                </router-link>   
                <v-btn flat>Help</v-btn>
            </v-toolbar-items>
        </div>

        <div>
            <v-navigation-drawer :mini-variant.sync="mini" v-model="drawer" stateless hide-overlay>
                <v-toolbar flat class="transparent">
                <v-list class="pa-0">
                    <v-list-tile avatar>
                    <v-list-tile-avatar>
                        <img src="https://randomuser.me/api/portraits/men/85.jpg" >
                    </v-list-tile-avatar>
                    <v-list-tile-content>
                        <v-list-tile-title>John Leider</v-list-tile-title>
                    </v-list-tile-content>
                    <v-list-tile-action>
                        <v-btn>
                        <v-icon>chevron_left</v-icon>
                        </v-btn>
                    </v-list-tile-action>
                    </v-list-tile>
                </v-list>
                </v-toolbar>
                <v-list class="pt-0" dense>
                <v-divider></v-divider>
                <v-list-tile v-for="item in items" :key="item.title">
                    <v-list-tile-action>
                    <v-icon>{{ item.icon }}</v-icon>
                    </v-list-tile-action>
                    <v-list-tile-content>
                    <v-list-tile-title>{{ item.title }}</v-list-tile-title>
                    </v-list-tile-content>
                </v-list-tile>
                </v-list>
            </v-navigation-drawer>
        </div>
    </v-toolbar>
</template>

<script>
  export default {
    data () {
      return {
        drawer: true,
        items: [
          { title: 'Home', icon: 'dashboard' },
          { title: 'About', icon: 'question_answer' }
        ],
        mini: true,
        right: null
      }
    }
  }
</script>
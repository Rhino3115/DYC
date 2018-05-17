<template>
    <v-container>
        <v-layout justify-center>
            <v-flex xs4>
                <v-avatar size="150">
                    <img src="@/assets/DYC-Logo (3).png" alt="dyclogo">
                </v-avatar>
                <v-form @submit="submit">
                    <v-text-field
                    v-model="email"
                    label="E-mail"
                    required
                    ></v-text-field>
                    
                    <v-text-field
                    v-model="password"
                    label="Password"
                    type="password"
                    required
                    ></v-text-field>
                    <v-btn>submit</v-btn>
                </v-form>
            </v-flex>
        </v-layout>
    </v-container>
</template>

<script>
export default {
  data(){
      return{
          email:null,
          password:null,
      }
  },
  methods:{
      submit(){
          console.log('hello')
      }
  },
}
</script>

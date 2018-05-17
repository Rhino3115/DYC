<template>
        <v-container mt-0>
            <v-layout justify-center>
                <v-flex xs3>
                    <div class="text-xs-center">
                        <v-avatar size="150">
                            <img src="@/assets/DYC-Logo (3).png" alt="dyclogo">
                        </v-avatar>
                    </div>
                    
                    <v-form @Login.prevent="submit">
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

                        <div class="text-xs-center">
                            <v-btn>Login</v-btn>
                        </div>
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

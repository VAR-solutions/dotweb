<template>
  <v-layout row wrap style="height: 100%">
    <v-flex xs12 sm6 md6 lg6 class="side">
        <v-card elevation="0" max-width="80%" class="mx-auto">
        <h1 class="pb-1 robob" style="color:black" >
         We would Love to<br>
         hear from you
      </h1>
      
      <p
        class="pt-3 robo"
      >In publishing and graphic design, lorem ipsum is a placeholder text commonly used to demonstrate the visual form of a document or a typeface without relying on meaningful content. Lorem ipsum may be used before final copy is available, but it may also be used to temporarily replace copy in a process called greeking, which allows designers to consider form without the meaning of the text influencing the design.</p>
        </v-card>
    </v-flex>





    <v-flex xs12 sm6 md6 lg6 style="background: #404040">
      <v-card style="color: #404040; align-content: center; justify-content:center" max-width="500">
        
          
          <v-form ref="form" align="center" >
            <v-text-field v-model="name" :counter="10" :rules="nameRules" label="Name" required></v-text-field>

            <v-text-field v-model="email" :rules="emailRules" label="E-mail" required></v-text-field>

            <v-text-field v-model="message" :counter="250" label="Message" required></v-text-field>

            

            <v-btn :disabled="!valid" color="success" class="mr-4" @click="validate">Validate</v-btn>

            <v-btn color="error" class="mr-4" @click="reset">Reset Form</v-btn>

            
          </v-form>
       
      </v-card>
    </v-flex>
  </v-layout>
</template>

<script>
export default {
  name: "Contact",
  data: () => ({
    name: "",
    nameRules: [
      v => !!v || "Name is required",
      v => (v && v.length <= 10) || "Name must be less than 10 characters"
    ],
    email: "",
    emailRules: [
      v => !!v || "E-mail is required",
      v => /.+@.+\..+/.test(v) || "E-mail must be valid"
    ],
  }),

  methods: {
    validate() {
     
    },
    reset() {
      this.$refs.form.reset();
    },
    
  }
};
</script>
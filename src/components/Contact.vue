<template>
  <v-layout row wrap style="height: 100%">
    <v-flex xs12 sm6 md6 lg6 class="d-flex align-center">
      <v-card elevation="0" max-width="80%" class="mx-auto">
        <h1 class="pb-1 robob siz" style="color:black">
          We would Love to
          <br />hear from you
        </h1>

        <p
          class="pt-3 robo siz1"
        >In publishing and graphic design, lorem ipsum is a placeholder text commonly used to demonstrate the visual form of a document or a typeface without relying on meaningful content. Lorem ipsum may be used before final copy is available, but it may also be used to temporarily replace copy in a process called greeking, which allows designers to consider form without the meaning of the text influencing the design.</p>
      </v-card>
    </v-flex>

    <v-flex xs12 sm6 md6 lg6 style="background: #404040">
      <v-card color="black my-5" width="80%" class="mx-auto">
        <v-row>
          <v-col cols="7" xs="6">
            <v-row>
              <v-col cols="2" xs="2" class="my-auto pa-0">
                <v-row justify="space-around">
                  <v-icon size="35" color="white">mdi-map-marker</v-icon>
                </v-row>
              </v-col>
              <v-col cols="10" xs="10" class="pa-0 my-auto">
                <p style="color: white; font-size: 0.8em">
                  Indian Institute of Information
                  <br />Technology, Vadodara
                  <br />Block No. 09, GEC Sector-28,
                  <br />Gandhinagar, Gujarat - 382028
                </p>
              </v-col>
            </v-row>
          </v-col>

          <v-col cols="5" xs="6" class="my-auto">
            <p style="color: white; font-size: 0.8em">
              <v-icon color="white">mdi-phone</v-icon>+91-7567775854
              <br />
              <v-icon color="white">mdi-email</v-icon>dot.iiitv@gmail.com
              <br />Follow us
              <v-icon size="20" color="white">mdi-basketball</v-icon>
              <v-icon size="20" color="white">mdi-linkedin</v-icon>
              <v-icon size="20" color="white">mdi-behance</v-icon>
            </p>
          </v-col>
        </v-row>
      </v-card>
      <v-card width="80%" class="mx-auto" color="black">
        <p class="ml-5 mb-1" style="color:white">Get in touch with us</p>
        <hr class="ml-5" style="color: white; border: 2px solid white; width: 10%;" />
        <v-form ref="form" class="mt-2">
          <v-row>
            <v-col cols="12" sm="10" class="ml-5">
              <v-text-field
                v-model="name"
                color="white"
                :rules="nameRules"
                label="Name"
                required
                placeholder="Name"
                background-color="white"
                height="8mm"
                dense="true"
              ></v-text-field>
            </v-col>
          </v-row>
          <v-row>
            <v-col cols="12" sm="10" class="ml-5">
              <v-text-field
                v-model="email"
                :rules="emailRules"
                color="white"
                label="E-mail"
                required
                placeholder="E-mail"
                background-color="white"
                height="8mm"
                dense="true"
              ></v-text-field>
            </v-col>
          </v-row>
          <v-row>
            <v-col cols="12" sm="10" class="ml-5 ">
              <v-textarea
                v-model="message"
                color="white"
                label="Message"
                required
                placeholder="Message"
                background-color="white"
                dense="true"
              ></v-textarea>
            </v-col>
          </v-row>
          <v-btn class="ml-5 mb-3" outlined color="white" @click="validate">Send</v-btn>

          <!-- <v-btn outlined color="red" @click="reset">Reset Form</v-btn> -->
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
    message: ""
  }),

  methods: {
    validate() {},
    reset() {
      this.$refs.form.reset();
    }
  }
};
</script>
<template>
  <v-layout row wrap style="height: 100%">
    <v-flex xs12 sm6 md6 lg6 class="d-flex align-center">
      <v-card elevation="0" max-width="80%" class="mx-auto">
        <h1 class="pb-1 robob siz" style="color:black">
          Meet our
          <br />Awesome Team
        </h1>

        <p
          class="pt-3 robo siz1"
        >In publishing and graphic design, lorem ipsum is a placeholder text commonly used to demonstrate the visual form of a document or a typeface without relying on meaningful content. Lorem ipsum may be used before final copy is available, but it may also be used to temporarily replace copy in a process called greeking, which allows designers to consider form without the meaning of the text influencing the design.</p>
      </v-card>
    </v-flex>
    <v-flex xs12 sm6 md6 lg6 style="height: 100% ; background: #404040">
      <v-container grid-list-sm align-content-space-between>
        <v-layout wrap>
          <v-flex v-for="k in 3" :key="k" xs4 sm4 md4>
            <v-card
              class="mx-auto mb-2"
              width="100%"
              tile
              elevation="0"
              style="background: #404040"
            >
              <v-dialog v-model="dialog" dark >
                <template v-slot:activator="{ on }">
                  <v-layout align-center justify-center pt-4>
                    <v-avatar size="100">
                      <img
                        v-on="on"
                        src="https://avataaars.io/?avatarStyle=Transparent&topType=ShortHairShortCurly&accessoriesType=Prescription02&hairColor=Black&facialHairType=Blank&clotheType=Hoodie&clotheColor=White&eyeType=Default&eyebrowType=DefaultNatural&mouthType=Default&skinColor=Light"
                      />
                    </v-avatar>
                  </v-layout>
                </template>
                hello from dialog
              </v-dialog>

              <p class="mt-3" justify="center" align="center" style="color: white">Name</p>

              <p
                style="font-size: 0.8em; margin-top: -8%; color:white"
                justify="center"
                align="center"
              >Designation</p>
            </v-card>
          </v-flex>
        </v-layout>
      </v-container>

      <hr class="mx-auto" style="color: white; border: 0.5px solid white; width: 80%;" />

      <Members />
    </v-flex>
  </v-layout>
</template>

<script>
import Members from "./Members";
export default {
  name: "Team",
  components: {
    Members
  },
  data() {
    return {
      dialog: false
    }

  }
};
</script>
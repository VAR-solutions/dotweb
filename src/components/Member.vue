<template>
  <v-card class="mx-auto mb-2" width="100%" tile elevation="0" style="background: #404040">
    <v-dialog v-model="dialog" dark>
      <template v-slot:activator="{ on }">
        <v-layout align-center justify-center pt-4>
          <v-avatar size="75">
            <img v-on="on"
              src="https://avataaars.io/?avatarStyle=Transparent&topType=ShortHairShortCurly&accessoriesType=Prescription02&hairColor=Black&facialHairType=Blank&clotheType=Hoodie&clotheColor=White&eyeType=Default&eyebrowType=DefaultNatural&mouthType=Default&skinColor=Light"
            />
          </v-avatar>
        </v-layout>
      </template>
      hello from dialog
    </v-dialog>
    <!-- <v-card-text class="mt-1" justify="center" align="center" style="color: white"> Name</v-card-text> -->
    <p class="mt-3" justify="center" align="center" style="color: white">Name</p>
  </v-card>
</template>

<script>
export default {
  data() {
    return {
      dialog: false
    };
  }
};
</script>
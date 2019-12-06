<template>
  <v-container grid-list-sm align-content-space-between>
    <v-layout>
      <v-flex xs3 md3 lg3>
        <Member />
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
import Member from "./Member";
export default {
  name: "Members",
  components: {
    Member
  }
};
</script>

<style>
.scroll {
  overflow-y: auto;
}
</style>
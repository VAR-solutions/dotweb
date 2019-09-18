<template>
  <v-container grid-list-sm align-content-space-between>
    <v-layout wrap>
      <v-flex v-for="k in 8" :key="k" xs3 sm3 md3>
        <Member />
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
import Member from './Member';
export default {
    name: "Members",
    components:{
        Member
    }
    
}
</script>
<template>
  <v-app>
    <v-app-bar title="Cabins Inc">
      <v-btn>About Us</v-btn>
    </v-app-bar>
<!--todo add side navbar-->
    <side-navbar></side-navbar>
    <v-main>
      <router-view>

      </router-view>
    </v-main>

  </v-app>
</template>
<script>
import SideNavbar from "@/components/SideNavbar";
export default {
  name: "GeneralLayout",
  components: {SideNavbar}
}
</script>

<style scoped>

</style>

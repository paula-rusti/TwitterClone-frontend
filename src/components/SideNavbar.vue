<template>
  <v-navigation-drawer
                       permanent
  >
    <v-list nav>
      <v-list-item prepend-icon="mdi-pound" title="Explore" to="/owner/profile"></v-list-item>
      <v-list-item prepend-icon="mdi-bell-outline" title="Notifications" to="/owner/profile"></v-list-item>
      <v-list-item prepend-icon="mdi-message-text-outline" title="Messages" to="/owner/profile"></v-list-item>
      <v-list-item prepend-icon="mdi-bookmark-outline" title="Bookmarks" to="/owner/profile"></v-list-item>
      <v-list-item prepend-icon="mdi-list-box-outline" title="Lists" to="/owner/profile"></v-list-item>
      <v-list-item prepend-icon="mdi-account" title="Profile" to="/owner/profile"></v-list-item>
      <v-list-item disabled="True" prepend-icon="mdi-more" title="More" to="/owner/profile"></v-list-item>
    </v-list>
  </v-navigation-drawer>
</template>

<script>
export default {
  name: "SideNavbar"
}
</script>

<style scoped>
.custom-list-item .custom-icon-size {
  font-size: 24px; /* Increase the icon size */
}

.custom-list-item .custom-title-size {
  font-size: 18px; /* Increase the title size */
}
</style>

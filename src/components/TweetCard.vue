<template>
  <v-card class="post-card">
    <v-card-title class="post-title">
      <v-avatar class="post-avatar">
        <img src="@/assets/elon.jpg" alt="Avatar">
      </v-avatar>
      <div class="post-user-info">
        <div class="user-details">
          <h3 class="post-username">John Doe</h3>
          <p class="post-time">10m</p>
        </div>
        <p class="post-handle">@johndoe</p>
      </div>
    </v-card-title>
    <v-card-text class="post-content">
      <p class="post-message">This is my awesome tweet! #Vuejs #Vuetify</p>
      <img src="@/assets/space.jpg" alt="Tweet Image" class="post-image">
    </v-card-text>
    <v-divider></v-divider>
    <v-card-actions class="post-actions">
      <v-btn icon>
        <v-icon>mdi-heart-outline</v-icon>
      </v-btn>
      <v-btn icon>
        <v-icon>mdi-share-variant</v-icon>
      </v-btn>
      <v-btn icon>
        <v-icon>mdi-message-outline</v-icon>
      </v-btn>
    </v-card-actions>
  </v-card>
</template>


<script>
export default {
  name: "TweetCard"
}
// todo establish card max height
</script>


<style scoped>
.post-card {
  max-width: 800px;
  margin: 0 auto;
  border-radius: 8px;
}

.post-title {
  padding: 16px;
  display: flex;
  align-items: center;
}

.post-avatar img {
  width: 48px;
  height: 48px;
}

.post-user-info {
  margin-left: 16px;
}

.user-details {
  display: flex;
  align-items: center;
}

.post-username {
  font-size: 16px;
  font-weight: bold;
  margin-bottom: 4px;
  margin-right: 15px;
}

.post-handle {
  font-size: 12px;
  color: gray;
}

.post-time {
  font-size: 12px;
  color: gray;
}

.post-content {
  padding: 16px;
}

.post-message {
  font-size: 14px;
  margin-bottom: 8px;
}

/*.post-image {*/
/*  width: 100%;*/
/*  max-height: 300px;*/
/*  object-fit: cover;*/
/*  border-radius: 8px;*/
/*}*/

.post-image {
  max-width: 100%;
  max-height: 100%;
  object-fit: contain;
  border-radius: 8px;
}

.post-actions {
  padding: 8px;
}
</style>




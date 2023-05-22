<template>
  <v-card class="who-to-follow-card">
    <v-card-title class="who-to-follow-card-title">
      <h3 class="who-to-follow-card-heading">Who to Follow</h3>
      <v-icon class="who-to-follow-card-settings">mdi-dots-vertical</v-icon>
    </v-card-title>
    <v-card-text class="who-to-follow-card-content">
      <div v-for="user in users" :key="user.id" class="user-item">
        <v-avatar class="user-avatar">
          <img src="@/assets/lex.jpg" alt="User Avatar">
        </v-avatar>
        <div class="user-details">
          <p class="user-name">{{ user.name }}</p>
          <p class="user-handle">{{ user.handle }}</p>
        </div>
        <v-btn class="follow-button" color="primary" outlined small>Follow</v-btn>
      </div>
    </v-card-text>
    <v-card-actions class="who-to-follow-card-actions">
      <v-btn class="refresh-button" icon>
        <v-icon>mdi-refresh</v-icon>
      </v-btn>
      <v-btn class="view-all-button" text>Show More</v-btn>
    </v-card-actions>
  </v-card>
</template>

<script>
export default {
  data() {
    return {
      users: [
        {
          id: 1,
          name: "John Doe",
          handle: "@johndoe",
          avatar: "@/assets/lex.jpg"
        },
        {
          id: 2,
          name: "Jane Smith",
          handle: "@janesmith",
          avatar: "@/assets/lex.jpg"
        },
        // Add more user objects as needed
      ]
    };
  }
};
</script>

<style scoped>
.who-to-follow-card {
  margin: 0 auto;
  border-radius: 8px;
}

.who-to-follow-card-title {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 16px;
}

.who-to-follow-card-heading {
  font-size: 18px;
  font-weight: bold;
  margin: 0;
}

.who-to-follow-card-settings {
  color: gray;
  font-size: 24px;
}

.who-to-follow-card-content {
  padding: 0 16px 16px;
}

.user-item {
  display: flex;
  align-items: center;
  margin-bottom: 12px;
}

.user-avatar img {
  width: 48px;
  height: 48px;
}

.user-details {
  margin-left: 12px;
}

.user-name {
  font-size: 16px;
  margin: 0;
}

.user-handle {
  font-size: 14px;
  color: gray;
  margin: 0;
}

.follow-button {
  margin-left: auto;
  padding: 6px 16px;
  text-transform: none;
}

.who-to-follow-card-actions {
  padding: 0 16px 16px;
}

.refresh-button {
  padding: 6px;
}

.view-all-button {
  text-transform: none;
}
</style>

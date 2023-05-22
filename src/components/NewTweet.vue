<template>
  <v-card class="new-tweet-card">
    <v-card-text class="new-tweet-card-content">
      <v-avatar class="new-tweet-avatar">
        <img src="@/assets/elon.jpg" alt="Avatar">
      </v-avatar>
      <div class="new-tweet-input">
        <textarea
          class="new-tweet-textarea"
          rows="4"
          placeholder="What's happening?"
        ></textarea>
      </div>
    </v-card-text>
    <v-card-actions class="new-tweet-card-actions">
      <v-btn class="new-tweet-action-button" icon>
        <v-icon>mdi-image</v-icon>
      </v-btn>
      <v-btn class="new-tweet-action-button" icon>
        <v-icon>mdi-file-gif-box</v-icon>
      </v-btn>
      <v-btn class="new-tweet-action-button" icon>
        <v-icon>mdi-poll</v-icon>
      </v-btn>
      <v-btn class="new-tweet-action-button" icon>
        <v-icon>mdi-emoticon-outline</v-icon>
      </v-btn>
      <v-btn class="new-tweet-action-button" icon>
        <v-icon>mdi-paperclip</v-icon>
      </v-btn>
      <v-spacer></v-spacer>
      <v-btn class="new-tweet-button" color="primary">Tweet</v-btn>
    </v-card-actions>
  </v-card>
</template>

<script>
export default {
  name: "NewTweet"
}
</script>



<style scoped>
.new-tweet-card {
  margin-bottom: 16px;
  border-radius: 12px;
  background-color: #f5f8fa;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.new-tweet-card-content {
  display: flex;
  padding: 16px;
}

.new-tweet-avatar img {
  width: 48px;
  height: 48px;
}

.new-tweet-input {
  flex-grow: 1;
  margin-left: 12px;
}

.new-tweet-textarea {
  width: 100%;
  border: none;
  resize: none;
  font-size: 16px;
  padding: 8px;
  outline: none;
  background-color: transparent;
  color: #14171a;
}

.new-tweet-card-actions {
  padding: 0 16px 16px;
}

.new-tweet-action-button {
  padding: 6px;
}

.new-tweet-button {
  padding: 8px 24px;
  border-radius: 9999px;
  text-transform: none;
}
</style>


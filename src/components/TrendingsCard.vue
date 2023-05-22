<template>
  <v-card class="trends-card">
    <v-card-title class="trends-card-title">
      <h3 class="trends-card-heading">Trends for you</h3>
      <v-icon class="trends-card-settings">mdi-dots-vertical</v-icon>
    </v-card-title>
    <v-card-text class="trends-card-content">
      <ul class="trends-list">
        <li v-for="trend in trends" :key="trend.id" class="trend-item">
          <p class="trend-name">{{ trend.name }}</p>
          <p class="trend-volume">{{ trend.volume }}</p>
        </li>
      </ul>
    </v-card-text>
    <v-card-actions class="trends-card-actions">
      <v-btn class="trends-card-action-button" color="primary">Show More</v-btn>
    </v-card-actions>
  </v-card>
</template>

<script>
export default {
  data() {
    return {
      trends: [
        { id: 1, name: "#TrendingTopic1", volume: "10.2K Tweets" },
        { id: 2, name: "#TrendingTopic2", volume: "8.6K Tweets" },
        { id: 3, name: "#TrendingTopic3", volume: "7.4K Tweets" },
        // Add more trend objects as needed
      ]
    };
  }
};
</script>

<style scoped>
.trends-card {
  margin: 0 auto;
  border-radius: 8px;
}

.trends-card-title {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 16px;
}

.trends-card-heading {
  font-size: 18px;
  font-weight: bold;
  margin: 0;
}

.trends-card-settings {
  color: gray;
  font-size: 24px;
}

.trends-card-content {
  padding: 16px;
}

.trends-list {
  list-style-type: none;
  padding: 0;
  margin: 0;
}

.trend-item {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 12px;
}

.trend-name {
  font-size: 16px;
  margin: 0;
}

.trend-volume {
  font-size: 14px;
  color: gray;
  margin: 0;
}

.trends-card-actions {
  padding: 8px;
}

.trends-card-action-button {
  text-transform: none;
}
</style>





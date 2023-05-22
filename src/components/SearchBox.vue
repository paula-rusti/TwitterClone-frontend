<template>
  <div class="search-box">
    <v-icon class="search-icon">mdi-magnify</v-icon>
    <input type="text" class="search-input" placeholder="Search on Twitter">
  </div>
</template>

<script>
export default {
  name: "SearchBox"
}
</script>

<style scoped>
.search-box {
  display: flex;
  align-items: center;
  background-color: #e6ecf0;
  border-radius: 24px;
  padding: 6px 12px;
}

.search-icon {
  font-size: 20px;
  color: #657786;
}

.search-input {
  flex-grow: 1;
  border: none;
  background-color: transparent;
  padding: 8px;
  font-size: 16px;
  outline: none;
  color: #14171a;
}
</style>





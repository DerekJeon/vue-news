<template>
  <div>
    <div v-for="user in users" v-bind:key="user"> {{ user }}</div>
  </div>
</template>

<script>
import { fetchNewsList } from '../api/index.js';

export default {
  data() {
    return {
      users: []
    }
  },
  created() {
    this.$store.dispatch('FETCH_NEWS');
  },
}
</script>

<style>

</style>
<template>
  <div>
    <h1>The User Page</h1>
    <hr>
    <p>Loaded ID: {{ id }}</p>
    <button @click="navigateToHome()">Go to Home</button>
    <hr>
    <router-view></router-view>
  </div>
</template>
<script>
export default {
  name: "User",
  data() {
    return {
        id: this.$route.params.id
    };
  },
  methods: {
    navigateToHome() {
      this.$router.push("/");
    }
  }
};
</script>
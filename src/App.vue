<template>
  <div class="content">
    <Card
      v-for="user in users"
      :key="user.id"
      :name="user.name.first"
      :mail="user.email"
      :phone="user.phone"
    />
  </div>
</template>

<script>
import Card from "./components/Card.vue";
import axios from "axios";

export default {
  name: "App",
  components: {
    Card,
  },

  data() {
    return {
      users: [],
    };
  },

  mountedclean() {
    axios
      .get(`https://randomuser.me/api/?results=12`)
      .then((response) => {
        this.users = response.data.results;
      })
      .catch((e) => {
        this.errors.push(e);
      });
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.content {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: repeat(3, 1fr);
  grid-column-gap: 0px;
  grid-row-gap: 20px;
}
</style>

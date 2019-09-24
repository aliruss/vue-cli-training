<template>
  <div id="app">
    <h1>{{ title }}</h1>
    <Navbar />
    <AllFriends :friends="friends" @listenerName="deleteFriend" />
    <OnlineFriends :friends="friends" />
  </div>
</template>

<script>
import Navbar from "./components/Navbar";
import AllFriends from "./components/AllFriends";
import OnlineFriends from "./components/OnlineFriends";
export default {
  name: "app",
  components: {
    Navbar,
    AllFriends,
    OnlineFriends
  },
  data() {
    return {
      title: "hello this is new file :)",
      friends: [
        { name: "Ali", online: true },
        { name: "Hsasan", online: false },
        { name: "Akbar", online: false },
        { name: "Sadegh", online: true }
      ]
    };
  },
  methods: {
    deleteFriend(e) {
      this.friends = this.friends.filter(friend => {
        return friend.name !== e.name;
      });
    }
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
h1 {
  text-align: center;
  color: #444;
}
</style>

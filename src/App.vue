<template>
  <div id="app">
    <TheHeader><h2>Check Out Our Games</h2></TheHeader>
    <nav>
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </nav>
    <router-view />
    <ol class="myList">
      <li v-for="item in sortList" v-bind:key="item.title">
        {{ item.title }}
      </li>
    </ol>
    <TheFooter />
  </div>
</template>

<script>
import TheHeader from "./components/TheHeader";
import TheFooter from "./components/TheFooter";
export default {
  data() {
    return {
      games: [
        { title: "Poker" },
        { title: "X-box" },
        { title: "Uno" },
        { title: "Beer pound" },
      ],
    };
  },
  computed: {
    sortList() {
      return [...this.games].sort(function (a, b) {
        let textA = a.title.toUpperCase();
        let textB = b.title.toUpperCase();
        return (textA < textB) ? -1 : (textA > textB) ? 1 : 0;
      });
    },
  },
  components: {
    TheHeader,
    TheFooter,
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
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
ol{
  list-style-type: none;
}
li{
  margin: 15px;
  font-size: 35px;
  color: aquamarine;
}

</style>

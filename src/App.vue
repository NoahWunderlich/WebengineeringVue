<template>
  <div>
  <nav style="background-color:gray;font-size:32px;font-family:arial;">
    <router-link to="/">Home</router-link> |    <router-link to="/timetableview">TimeTable</router-link> | 
    <router-link to="/twitterview">Twitter</router-link> | 
    <router-link to="/adminview">Admin</router-link>
  </nav>
  <div class="grey lighten-4 backImg">
      <router-view />
  </div>
  </div>
</template>

<style lang="scss">
  *{
    margin:0px;

  }
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: blue;
    }
  }
}
</style>

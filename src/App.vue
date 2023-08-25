<template>

  <router-view/>
</template>

<style>
:root{
    --green: #90ee90;
    --greentea: #CEDEBD;
    --light: #f5f5f5;
    --dark: #27374D;
    --grey: #61677A;
    --darker: #040D12;
    --sidebar-width: 300px;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;

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
</style>

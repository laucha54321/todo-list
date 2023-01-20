<template>
  <RouterView></RouterView>
</template>
<style scoped>

@import url('https://fonts.googleapis.com/css2?family=Roboto+Condensed:wght@300;400;700&display=swap');
*{
  margin:0;
  padding: 0;
  list-style: none;
  text-decoration: none;
  font-family: 'Roboto Condensed', sans-serif;
}
body{
  background-color: aqua;
}
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>

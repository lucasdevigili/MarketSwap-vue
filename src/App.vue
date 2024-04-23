<template>
  <router-view />
</template>

<style>
* {
  margin: 0;
  padding: 0;
}

body {
  font-family: "Inter", sans-serif;
}

.button,
button,
li {
  cursor: pointer;
}

.fab,
button {
  box-shadow: 0px 4px 10px -8px rgba(0, 0, 0, 1);
  transition: .5s;
}

.fab:hover,
button:hover {
  box-shadow: 0px 4px 10px -2px rgba(0, 0, 0, .5);
  transition: .5s;
}
</style>

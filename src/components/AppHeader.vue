<template>
  <header class="header">
    <!-- <img class="logo" src="path-to-logo.png" alt="Logo" /> -->
    <p>logo</p>
    <nav>
      <ul>
        <li><a href="#" class="navItem">Home</a></li>
        <li><a href="#" class="navItem">About</a></li>
        <li><a href="#" class="navItem">Pricing</a></li>
        <li><a href="#">Blog</a></li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: 'AppHeader'
}
</script>

<style scoped>
a{
  /* text-decoration: none; */
  /* color: black; */

  padding-right: 1rem;
}

.navItem{
  border-right: black 2px solid;
}
.header {
  height:10vh;
  padding: .5rem .8rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
  background-color: rgb(248, 249, 249);
}

/* .logo {
    height: 7rem;
    width: 7rem;
  } */
nav ul {
  list-style-type: none;
  display: flex;
  gap: 1rem;
}
</style>
  
<template>
  <header>
    <nav>
      <ul>
        <li>
          <nuxt-link to="/">Starting Page</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/recipes">Recipes</nuxt-link>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {};
</script>

<style scoped>
header {
  width: 100%;
  height: 30px;
  margin: 10px 0;
  display: flex;
  justify-content: center;
  align-items: center;
  background: black;
}

ul {
  list-style: none;
  padding: 0;
  margin: 0;
  display: flex;
  justify-content: center;
  align-items: center;
}

li {
  margin: 0 10px;
  flex-grow: 1;
}

li a {
  text-decoration: none;
  color: white;
  padding: 10px;
}

li a:hover {
  color: black;
  background: white;
  display: inline-block;
  font-style: bold;
}
</style>
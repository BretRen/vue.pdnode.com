<template>
  <nav class="nav">
    <h1 class="logo">Pdnode Team</h1>
    <ul class="menu">
      <li><a href="/">Home</a></li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: "Nav",
};
</script>

<style scoped>
.nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0; /* 或少量 padding，如 0.5rem */
  background: transparent; /* 透明 */
  box-shadow: none; /* 去掉阴影 */
  margin-right: 2rem;
}


@media (min-width: 768px) {
  .nav {
    flex-direction: row;
  }
}

.logo {
  color: #2563eb;
  font-size: 1.5rem;
  font-weight: bold;
  margin-bottom: 0.5rem;
  margin-left: 0.5rem;
}

.menu {
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
  list-style: none;
  padding: 0;
  margin: 0;
  align-items: center;
  font-weight: 600;
}

@media (min-width: 768px) {
  .menu {
    flex-direction: row;
    gap: 1.5rem;
  }
}

.menu a {
  color: #444;
  text-decoration: none;
  transition: color 0.2s;
}

.menu a:hover {
  color: #2563eb;
}
</style>

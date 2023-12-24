<template>
  <nav id="menu">
    <ul>
      <li>
        <router-link to="/">mathilde dewawrin</router-link>
      </li>
      <li>
        <router-link to="/about">projects</router-link>
      </li>
      <li>
        <router-link to="/about">About</router-link>
      </li>
    </ul>
  </nav>
  <router-view />
</template>

<style lang="scss">
html,
body {
  padding: 0 !important;
  margin: 0 !important;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 0px;
}

nav {
  font-family: var(--font-systeme);
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  padding: 16px;
  ul {
    list-style: none;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    width: 100%;
    li {
      flex-basis: 100%;
    }
    padding-left: 0px;
  }
  ul li:first-child {
    text-align: left;
  }
  ul li:last-child {
    text-align: right;
  }
  position: fixed;
  top: 0px;
  width: calc(100% - 32px);
  a {
    text-decoration: none;
    color: #000;
    font-size: 16px;
    font-style: normal;
    font-weight: 600;
    line-height: 24px; /* 200% */
    letter-spacing: 0.24px;
  }
}
</style>

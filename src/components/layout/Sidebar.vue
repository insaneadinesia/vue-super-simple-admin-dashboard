<template>
  <nav id="sidebar">
    <ul class="nav flex-column">
      <li class="nav-item">
        <router-link
          class="nav-link active"
          to="/">
          Dashboard
        </router-link>
      </li>
      <li class="nav-item" ref="about">
        <span
          @click="toggleCollapse('about')"
          class="nav-link">
          About
        </span>

        <ul class="nav flex-column subnav">
          <li class="nav-item">
            <router-link
              to="/"
              class="nav-link">
              Index
            </router-link>
          </li>
          <li class="nav-item">
            <router-link
              to="/"
              class="nav-link">
              Sub menu
            </router-link>
          </li>
          <li class="nav-item">
            <router-link
              to="/"
              class="nav-link">
              Sub menu
            </router-link>
          </li>
          <li class="nav-item">
            <router-link
              to="/"
              class="nav-link">
              Sub menu
            </router-link>
          </li>
        </ul>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#">Items</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#">Users</a>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  methods: {
    toggleCollapse(item) {
      if (item === 'about') {
        return this.$refs.about.classList.toggle('open');
      }

      return true;
    },
  },
};
</script>

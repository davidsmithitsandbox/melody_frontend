<template>
  <nav id="nav-bar-top" class="navbar navbar-expand-lg navbar-light bg-light">
    <a class="navbar-brand" href="/">Melody</a>
    <button
      class="navbar-toggler"
      type="button"
      data-toggle="collapse"
      data-target="#navbarNav"
      aria-controls="navbarNav"
      aria-expanded="false"
      aria-label="Toggle navigation"
    >
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav">
        <li class="nav-item active">
          <router-link
            to="Home"
            v-slot="{ href, route, navigate, isActive, isExactActive }"
          >
            <NavLink
              :class="'nav-link'"
              :active="isActive"
              :href="href"
              @click="navigate"
              >{{ route.fullPath }}</NavLink
            >
          </router-link>
        </li>
        <li class="nav-item">
          <router-link :class="'nav-link'" :to="{ name: 'users' }"
            >Users</router-link
          >
        </li>
      </ul>
    </div>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      LogoContent: "Logos"
    };
  }
};
</script>

<style></style>

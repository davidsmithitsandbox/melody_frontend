<template>
  <div id="app">
    <div id="nav">
      <router-link :to="{ name: 'home' }">Home</router-link>|
      <router-link :to="{ name: 'users' }">Users</router-link>|
      <router-link
        :to="{
          name: 'users-show',
          params: {
            username: 'Tom'
          }
        }"
        >Tom</router-link
      >
    </div>
    <router-view />
  </div>
</template>

<style></style>

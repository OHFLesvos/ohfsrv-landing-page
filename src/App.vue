<template>
  <div id="app" class="container align-self-center">
    <div class="card">
      <img alt="Logo" src="./assets/logo.png" class="card-img-top px-4 py-3" />
      <div class="card-body">
        <h5 class="card-title text-center">
          Welcome to the OHF content server
        </h5>
        <p class="card-text text-center">
          Please select an application from the list below:
        </p>
      </div>
      <div class="list-group list-group-flush">
        <a
          v-for="(link, idx) in links"
          :key="idx"
          :href="link.url"
          class="list-group-item list-group-item-action text-center"
        >
          {{ link.label }}
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      links: [
        {
          label: "phpMyAdmin",
          url: "/phpmyadmin",
        },
        {
          label: "Cockpit",
          url: "https://ohfsrv01:9090",
        },
        {
          label: "Kiwix",
          url: "http://ohfsrv01:8002",
        },
      ],
    };
  },
};
</script>

<style scoped>
#app {
  max-width: 500px;
}
</style>
<template>
  <main>
    <div class="search">
      <input
        type="text"
        name="search"
        placeholder="Search for a city..."
        autocomplete="off"
      />
    </div>

    <div class="wrapper">
      <div class="location">
        Tampa, FL
      </div>
      <div class="date">
        Thursday May 21, 2020
      </div>

      <div class="weather">
        <div class="temp">81 degrees</div>
        <div class="climate">Sunny</div>
      </div>
    </div>
  </main>
</template>

<script>
  export default {
    name: "weather",

    data() {
      return {
        api_key: "9d32b0c4372889caf6edfda19dabe8fb",
      };
    },
  };
</script>

<style></style>

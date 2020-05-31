<template>
  <div id="app">
    <Weather></Weather>
  </div>
</template>

<script>
import Weather from "./components/Weather";

export default {
  name: "App",
  components: {
    Weather
  }
};
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

#app {
  font-family: "Montserrat", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  background-image: url("./assets/cold.jpg");
  background-size: cover;
  background-position: bottom;
  transition: 0.4s;
}

main {
  min-height: 100vh;
  padding: 2rem;
  background-image: linear-gradient(
    to bottom,
    rgba(0, 0, 0, 0.25),
    rgba(0, 0, 0, 0.75)
  );

  .wrapper {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin-top: 8rem;
    color: #fff;
    text-align: center;
    font-size: 2rem;
    text-shadow: 0.25rem 0.5rem rgba(0, 0, 0, 0.25);

    .date {
      font-size: 1.5rem;
      font-style: italic;
    }
  }

  .weather {
    .temp {
      display: inline-block;
      padding: 0.6rem 1rem;
      font-size: 5rem;
      font-weight: 900;
      background: rgba(255, 255, 255, 0.25);
      border-radius: 1rem;
      margin: 1.5rem 0;
      box-shadow: 0 0.5rem 0.5rem rgba(0, 0, 0, 0.5);
    }

    .climate {
      font-size: 1.5rem;
      font-weight: 700;
      font-style: italic;
      text-shadow: 0.1rem 0.1rem rgba(0, 0, 0, 0.25);
    }
  }
}

.search {
  width: 100%;
  margin-bottom: 2rem;
  display: flex;
  justify-content: center;

  input {
    width: 50%;
    padding: 1rem;

    color: #fff;
    text-shadow: 0.15rem 0.15rem 0.15rem #000;
    font-size: 1.4rem;
    appearance: none;
    border: 0.1rem solid #000;
    border-radius: 1rem 0 1rem 0;
    outline: none;
    background: none;
    background-color: rgba(255, 255, 255, 0.15);
    transition: 0.3s ease;
    box-shadow: 0 0 0.5rem rgba(0, 0, 0, 0.25);

    &::-webkit-input-placeholder {
      /* Chrome/Opera/Safari */
      color: #fff;
    }

    &:focus {
      border: 0.1rem solid #fff;
      box-shadow: 0 0 1rem rgba(0, 0, 0, 0.25);
      border-radius: 0 1rem 0 1rem;
    }
  }
}
</style>

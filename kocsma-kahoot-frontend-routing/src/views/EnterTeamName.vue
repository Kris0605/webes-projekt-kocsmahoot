<template>
  <div>
    <h2>{{ $route.params.name }}</h2>
    <h2>Enter the name of your team!</h2>
    <div id="teamname-enter-form">
      <div>
        <input type="text" />
        <button @click="SetGameStarted">
          <router-link
            style="text-decoration: none"
            :to="{ name: 'WaitingForGameStartAdmin' }"
            >GO!</router-link
          >
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {},
  methods: {
    SetGameStarted() {
      this.$store.commit("setGameStarted");
    },
  },
  data() {
    return {};
  },
};
</script>

<style scoped>
#teamname-enter-form {
  display: block;
  margin: auto;
  width: 60%;
  padding-bottom: 50px;
}

#teamname-enter-form div{
  display: flex;
  justify-content:center
}

input {
  flex: 5;
  height: 100px;
  width: 500px;
  font-size: 80px;
  margin-top: 0;
  margin-bottom: 0;
  margin-right: 10px;
  padding-top: 0;
  padding-bottom: 0;
}

button {
  flex: 1;
  height: 100px;
  min-width: 150px;
  font-size: 50px;
  font-weight: bold;
  margin-top: 0;
  margin-bottom: 0;
  padding-top: 0;
  padding-bottom: 0;
  background-color: darkred;
  text-align: center;
}

a {
  color: white;
}
</style>

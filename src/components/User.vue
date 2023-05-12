<template>
  <h1>User Component</h1>
  <button v-on:click="getUser(userName)">Send User Name to Parent</button>
</template>
<script>
export default {
  name: "MyUser",
  props: {
    getUser: Function,
  },
  data() {
    return {
      userName: "Mukta",
    };
  },
};
</script>

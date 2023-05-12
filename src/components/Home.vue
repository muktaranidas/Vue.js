<template>
  <h1>Simple Form</h1>
  <!-- <p>{{ form }}</p> -->
  <ul>
    <li v-for="item in error" v-bind:key="item">{{ item }} is not Valid</li>
  </ul>
  <form>
    <label> Email: </label>
    <input type="text" placeholder="enter email" v-model="form.email" />
    <br />
    <br />

    <label> Password: </label>
    <input
      type="password"
      placeholder="enter password"
      v-model="form.password"
    />
    <br />
    <br />

    <select v-model="form.country">
      <option>Bangladesh</option>
      <option>Canada</option>
    </select>
    <br />
    <br />

    <h3>Gender</h3>
    <label>Male: </label>
    <input type="radio" name="gender" value="male" v-model="form.gender" />
    <br />
    <br />

    <label>Female: </label>
    <input type="radio" name="gender" value="female" v-model="form.gender" />
    <br />
    <br />

    <h3>Technology</h3>
    <label>JavaScript : </label>
    <input type="checkbox" value="javascript" v-model="form.technology" />
    <br />
    <br />
    <label>React : </label>
    <input type="checkbox" value="react" v-model="form.technology" />
    <br />
    <br />

    <button v-on:click="login" type="button">Login</button>
  </form>
</template>

<script>
export default {
  name: "MyHome",
  data() {
    return {
      form: {
        email: "",
        password: "",
        country: "",
        gender: "",
        technology: [],
      },
      error: [],
    };
  },
  methods: {
    login() {
      this.error = [];
      for (const item in this.form) {
        if (this.form[item] === "" || this.form[item].length === 0) {
          this.error.push(item);
        }
      }
      if (this.error.length === 0) {
        alert("Data has been submitted");
      }
      console.warn(this.error);
    },
  },
};
</script>

<template>
  <h1>Props in Vue js 3</h1>

  <Student :name="name"></Student>
  <Teacher name="Rakib"></Teacher>
</template>
<script>
import Student from "./Student.vue";
import Teacher from "./Teacher.vue";
export default {
  name: "MyHome",
  components: {
    Student,
    Teacher,
  },

  data() {
    return {
      name: "Mukta",
    };
  },
};
</script>
<style>
h1 {
  color: orange;
}
</style>

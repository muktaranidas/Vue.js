<template>
  <h2>Teacher Name is: {{ name }}</h2>
</template>
<script>
export default {
  name: "MyTeacher",
  props: {
    name: String,
  },
};
</script>
<style></style>

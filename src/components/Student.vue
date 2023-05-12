<template>
  <h2>Student Name is: {{ name }}</h2>
</template>
<script>
export default {
  name: "MyStudent",
  props: {
    name: String,
  },
};
</script>

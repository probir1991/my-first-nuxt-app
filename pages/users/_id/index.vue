<template>
  <h1>Dynamic user ID: {{ $route.params.id }}</h1>
</template>

<script>
export default {
  validate(data) {
    console.log(data);
    //return data.params.id == 1;
    return /^\d+$/.test(data.params.id);
  },
  layout: "users"
};
</script>


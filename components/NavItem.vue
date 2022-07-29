<template>
  <div>
    <b-nav-item v-if="isActive == true">
      <NuxtLink :to="toPage"
        ><a class="nav-link active">{{ text }}</a></NuxtLink
      >
    </b-nav-item>
    <b-nav-item v-else>
      <NuxtLink :to="toPage"
        ><a class="nav-link">{{ text }}</a></NuxtLink
      >
    </b-nav-item>
  </div>
</template>

<script>
export default {
  props: {
    isActive: Boolean,
    text: String,
    toPage: String,
  },
};
</script>

<style lang="scss" scoped></style>

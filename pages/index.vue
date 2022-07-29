<template>
  <div>
    <Navbar :homeActive="true" :geometryActive="false" />
    <Header />
    <MenuList class="px-5 py-5" />
    <Footer class="mt-5" />
  </div>
</template>

<script>
export default {
  name: "IndexPage",
};
</script>

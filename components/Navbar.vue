<template>
  <div>
    <!-- Navbar -->
    <div>
      <b-navbar toggleable="lg" type="light" variant="light">
        <b-navbar-brand href="#">My Math Bakery 🍪</b-navbar-brand>

        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <b-collapse id="nav-collapse" is-nav>
          <b-navbar-nav>
            <NavItem text="Home" :isActive="homeActive" toPage="/" />

            <NavItem
              text="Geometry & Calculation"
              :isActive="geometryActive"
              toPage="/geometry"
            />
          </b-navbar-nav>

          <!-- Right aligned nav items -->
          <b-navbar-nav class="ml-auto"></b-navbar-nav>
        </b-collapse>
      </b-navbar>
    </div>
    <!-- Navbar -->
  </div>
</template>

<script>
export default {
  props: {
    homeActive: Boolean,
    geometryActive: Boolean,
  },
};
</script>

<style lang="scss" scoped></style>

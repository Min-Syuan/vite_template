<template>
    <header>
        <div class="wrapper">
            <nav>
              <RouterLink to="/">Home</RouterLink>
              <RouterLink to="/about">About</RouterLink>
              <RouterLink to="/product">Product</RouterLink>
              <RouterLink to="/login">login</RouterLink>
            </nav>
        </div>
    </header>
</template>

<script>
export default {
  data() {
    return {
      targetValue: 0
    }
  },
  created() {},
  methods: {}
}
</script>

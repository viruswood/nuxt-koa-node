<template>
  <section class="container">
    <div>
      <el-button type="text" @click="gotoMenu('/table')">table</el-button>
      <el-button type="text" @click="gotoMenu('/files')">file</el-button>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {}
  },
  methods: {
    gotoMenu(path) {
      this.$router.push({ path: path })
    }
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>

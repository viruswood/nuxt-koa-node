<template>
  <div>
    <el-container>
      <el-header height="50px" class="header">
        <!-- Header content -->
      </el-header>

      <el-container>
        <el-aside width="200px" class="aside">
          <!-- Aside content -->
        </el-aside>
        <el-main class="main">
          <!-- Main content -->
          <nuxt/>
        </el-main>
      </el-container>
    </el-container>
  </div>
</template>
<script>
export default {
  data() {
    return {}
  }
}
</script>
<style lang="scss" scoped>
.header {
  background-color: #369;
  padding: 0px;
}
.aside {
  background-color: #963;
  padding: 0px;
}
.main {
  height: calc(100vh - 50px);
  padding: 0px;
  // background-color: #f3f4f3;
}
</style>

<template>
  <el-container style="border: 1px solid #eee">
      <el-main>
        <el-row :gutter="20">
          <el-col :span="14"><div class="grid-content left-top"></div></el-col>
          <el-col :span="10"><div class="grid-content right-top"></div></el-col>
          <el-col :span="10"><div class="grid-content right-mid"></div></el-col>
        </el-row>
        <el-row :gutter="20">
          <el-col :span="14"><div class="grid-content left-bottom"></div></el-col>
          <el-col :span="10"><div class="grid-content right-bottom"></div></el-col>
        </el-row>
      </el-main>
  </el-container>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home'
}
</script>

<style>

.left-top {
  background: #99a9bf;
  height: 500px;
}
.left-bottom {
  background: #d3dce6;
  height: 240px;
}
.right-bottom {
  background: #e5e9f2;
  height: 240px;
}
.right-top{
  background: #42b983;
  height: 240px;
}
.right-mid{
  background: blue;
  height: 240px;
  margin-top: 20px;
}
.grid-content {
  border-radius: 4px;
  min-height: 36px;
}

</style>

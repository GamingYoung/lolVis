<template>
  <el-container style="border: 1px solid #eee">
      <el-main>
        <el-row :gutter="20">
          <el-col :span="12"><div class="grid-content left-top">
            <p class="abc">英雄克制关系</p>
            <iframe width="100%" height="800" frameborder="0"
                    src="https://observablehq.com/embed/b90394082b68af06@169?cells=viewof+message%2Cchart"></iframe>
          </div></el-col>
          <el-col :span="12"><div class="grid-content right-top">
            <p class="abc">强势英雄对局概览</p>
            <iframe width="100%" height="800" frameborder="0"
                    src="https://observablehq.com/embed/d6d13a3191898390@340?cells=viewof+message%2Cchart"></iframe>
          </div></el-col>
        </el-row>
        <el-row :gutter="20">
          <el-col :span="12"><div class="grid-content left-bottom">
            <p class="abc">版本更新英雄强度变化</p>
            <iframe width="100%" height="285" frameborder="0"
                    src="https://observablehq.com/embed/183a422d9b46f2e1?cells=chart"></iframe>
          </div></el-col>
          <el-col :span="12"><div class="grid-content right-bottom">
            <div class="block">
              <!--              <span class="demonstration">Click 指示器触发</span>-->
              <el-carousel trigger="click" height="285">
                <el-carousel-item v-for="item in list" :key="item">
                  <div class="wheel">
                    <img :src="item.imgPath" class="image">
                  </div>
                </el-carousel-item>
              </el-carousel>
            </div>
          </div></el-col>
        </el-row>
      </el-main>
  </el-container>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  data () {
    return {
      list: [
        {
          imgPath: 'https://shp.qpic.cn/cfwebcap/0/cfed6c6aa1f8a5eff65aca4da069bdbc/0/?width=1920&height=1080',
          url: 'https://shp.qpic.cn/cfwebcap/0/cfed6c6aa1f8a5eff65aca4da069bdbc/0/?width=1920&height=1080'
        },
        {
          imgPath: 'https://ossweb-img.qq.com/upload/webplat/info/lol/20221116/25397586155156.jpg',
          url: 'https://ossweb-img.qq.com/upload/webplat/info/lol/20221116/25397586155156.jpg'
        },
        {
          imgPath: 'https://ossweb-img.qq.com/upload/webplat/info/lol/20221102/391851488077693.jpg',
          url: 'https://ossweb-img.qq.com/upload/webplat/info/lol/20221102/391851488077693.jpg'
        }
      ]
    }
  }
}
</script>

<style>

.abc{
  text-align: center;
}
.left-top {
  background: #e5e9f2;
}
.left-bottom {
  background: #d3dce6;
  height: 300px;
  margin-top: 20px;
}
.right-bottom {
  background: #e5e9f2;
  height: 300px;
  margin-top: 20px;
}
.right-top{
  background: #e5e9f2;
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
.el-carousel__item h3 {
  color: #475669;
  font-size: 14px;
  opacity: 0.75;
  line-height: 150px;
  margin: 0;
}
.wheel{
  width: 100%;
  /*background: #f2f2f2;*/
  display: flex;
  justify-content: center;
  align-items: center;
}
.image{
  max-width: 100%;
  /*max-height: 700px;*/
}

</style>

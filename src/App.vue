<template>
  <div class="container">
    <div class="imglist">
      <h3>图片列表区</h3>
      <!-- 给鼠标添加鼠标进入事件，并给函数添加实参 -->
      <img
        src="./assets/01.jpg"
        alt=""
        @mouseover="imgFn(1)"
        @click="addFn(1, $event)"
      />
      <img
        src="./assets/02.jpg"
        alt=""
        @mouseover="imgFn(2)"
        @click="addFn(2, $event)"
      />
      <img
        src="./assets/03.jpg"
        alt=""
        @mouseover="imgFn(3)"
        @click="addFn(3, $event)"
      />
    </div>
    <div class="show">
      <h3>图片预览区</h3>
      <!-- 需要用v-bind -->
      <img :src="current" alt="" style="width: 600px; height: auto" />
    </div>
    <div></div>
  </div>
</template>

<script>
//引入图片
import img01 from './assets/01.jpg';
import img02 from './assets/02.jpg';
import img03 from './assets/03.jpg';
export default {
  name: 'App',
  data() {
    return {
      //给current设置默认值
      current: img01,
    };
  },
  methods: {
    imgFn(val) {
      //让current拿到对应得地址
      this.current = { 1: img01, 2: img02, 3: img03 }[val];
    },
    addFn(val, e) {
      console.log(val);
      alert(`第${val}张图${e.target.src}`);
    },
  },
};
</script>

<style scoped>
.container {
  display: flex;
}
.imglist {
  border: 2px solid red;
}
.imglist img {
  width: 200px;
  height: auto;
}
.show {
  border: 2px solid red;
  margin-right: 20px;
}
</style>

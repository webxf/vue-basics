<template>
  <div>
    <a :href="xf">百度一下</a>
    <img :src="imgUrl" />
    <img :src="imgLocal" />
  </div>
</template>

<script>
import imgLocal from './assets/logo.png';
export default {
  name: 'App',
  data() {
    return {
      xf: 'http://www.baidu.com',
      imgUrl:
        'http://yun.itheima.com/Upload/./Images/20210412/60741c11ab77b.jpg',
      imgLocal,
    };
  },
};
</script>

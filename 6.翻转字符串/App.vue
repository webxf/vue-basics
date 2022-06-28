<template>
  <div>
    <h2>{{ msg }}</h2>
    <button @click="btnFn">点我翻转</button>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      msg: 'hello,vue',
    };
  },
  methods: {
    btnFn() {
      //将字符串转化成数组
      this.msg = this.msg.split('').reverse().join('');
      // console.log(arr);
      //翻转数组，会改变原数组
      // console.log(arr.reverse());
      // console.log(arr.join(''));
      //将数组转化成字符串
      // this.msg = arr.join('');
    },
  },
};
</script>

<template>
  <div>
    <input type="text" v-model="val" />
    <br />
    <!-- 实现v-model 
    数据得到视图
      视图得到数据
      输入事件，输入过程中，实时拿到dom input里面的value值-->
    <input type="text" :value="val1" @input="iptFn" />
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      val: '',
      val1: '',
    };
  },
  methods: {
    iptFn(e) {
      this.val1 = e.target.value;
    },
  },
};
</script>

<template>
  <div>
    <!-- 
    	v-model:是实现vuejs 变量和表单标签value属性, 双向绑定的指令
    -->
    <!-- .number 以parseFloat转成数字类型
          .trim  去除首尾空白字符
          .lazy 在change时触发而非inupt时  -->
    <div>
      <input type="text" v-model.number="username" />
    </div>
    <div>
      <input type="text" v-model.trim="pass" />
    </div>

    <div>
      <textarea v-model.lazy="intro"></textarea>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      username: '',
      pass: '',
      intro: '',
    };
  },
};
</script>

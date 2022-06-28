<template>
  <div>
    <!-- 输入回车键触发事件 -->
    <input type="text" @keydown.enter="enterFn" />
    <br />
    <!-- 输入esc触发事件 -->
    <input type="text" @keydown.esc="escFn" />
  </div>
</template>

<script>
export default {
  name: 'App',

  methods: {
    enterFn() {
      alert('输入回车键');
    },
    escFn() {
      alert('输入了esc键');
    },
  },
};
</script>

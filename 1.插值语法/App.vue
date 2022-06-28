<template>
  <div>
    {{ msg }}
    <h1>{{ obj.uname }}</h1>
    <h1>{{ obj.age > 18 ? '成年' : '未成年' }}</h1>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      msg: '阿金',
      obj: {
        uname: '阿帆',
        age: 19,
      },
    };
  },
};
</script>

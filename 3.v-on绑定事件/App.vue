<template>
  <div>
    <h1>{{ count }}</h1>
    <button @click="count++">点我+1</button>
    <button @click="addFn">点我+1</button>
    <button @click="addFive(5)">点我+5</button>
    <button @click="subFn">点我-1</button>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      count: 0,
    };
  },
  methods: {
    addFn() {
      this.count++; //this指向vc
    },
    addFive(val) {
      this.count += val;
    },
    subFn() {
      this.count--;
    },
  },
};
</script>

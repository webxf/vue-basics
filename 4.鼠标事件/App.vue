<template>
  <div @click="fn">
    <!-- vue对事件进行了事件修饰符得设置，在事件后面，修饰符名即可使用更多的功能 -->
    <span @click.stop="sonFn">stop阻止冒泡</span>
    <!-- 可以连着写，既阻止默认行为也阻止冒泡了 -->
    <a @click.prevent.stop href="http://www.baodi.com">阻止去百度</a>
    <span @click.prevent>.prevent阻止默认行为</span>
    <span @click.once="btn">去百度</span>
  </div>
</template>

<script>
export default {
  name: 'App',

  methods: {
    btn() {
      console.log('a');
    },
    fn() {
      console.log('11');
    },
    sonFn() {
      console.log('12');
    },
  },
};
</script>

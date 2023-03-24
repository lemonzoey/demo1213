<template>
  <h1>{{ msg }}</h1>
  <button @click="count++">count is: {{ count }}</button>
  <p>
    Edit <code>components/HelloWorld.vue</code> to test hot module replacement.
  </p>
</template>

<script>
import lodash from 'lodash';
export default {
  name: 'HelloWorld',
  props: {
    msg: String,
  },
  data() {
    return {
      count: 0,
    };
  },
  created() {
    const base = {
      aps1: {
        host: '111',
        re: '222',
      },
    };
    const conf = {
      aps1: {
        ccc: '333',
        host: '444',
      },
    };

    const obj = {
      aps1: {
        host: '555',
        re: '555',
      },
    };
    const aa = lodash.defaultsDeep(conf, base, obj);
    // const bb = Object.assign(conf,base,obj)
    console.log('🚀 ~ file: HelloWorld.vue:32 ~ created ~ aa', aa);
  },
};
</script>

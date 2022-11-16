<!--
 * @Author: lujiayu lujiayu@shiqiao.com
 * @Date: 2022-11-14 20:25:18
 * @LastEditors: lujiayu lujiayu@shiqiao.com
 * @LastEditTime: 2022-11-16 17:28:46
 * @FilePath: /vue3.0-test/vue3-demo/src/components/HelloWorld.vue
 * @Description: 这是默认设置,请设置`customMade`, 打开koroFileHeader查看配置 进行设置: https://github.com/OBKoro1/koro1FileHeader/wiki/%E9%85%8D%E7%BD%AE
-->
<template>
  <h1>{{ msg }}</h1>
  <button @click="count++">count is: {{ count }}</button>
  <p>Edit <code>components/HelloWorld.vue</code> to test hot module replacement.</p>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return {
      count: 0
    }
  }
}
</script>

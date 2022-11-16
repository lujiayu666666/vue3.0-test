<!--
 * @Author: lujiayu lujiayu@shiqiao.com
 * @Date: 2022-11-14 20:25:18
 * @LastEditors: lujiayu lujiayu@shiqiao.com
 * @LastEditTime: 2022-11-16 20:41:15
 * @FilePath: /vue3.0-test/vue3-demo/src/components/HelloWorld.vue
 * @Description: 这是默认设置,请设置`customMade`, 打开koroFileHeader查看配置 进行设置: https://github.com/OBKoro1/koro1FileHeader/wiki/%E9%85%8D%E7%BD%AE
-->
<template>
  ref标题：{{title}}
  <br>
  <br>
  reactive个人信息：{{userInfo}}
  <br>
  <br>
  <button @click="getUserName()">获取reactive对象名字</button>

  <br>
  <br>
  <button @click="getTitle()">获取ref标题</button>

  <br>
  <br>
  <button @click="setTitle()">设置ref标题</button>

  <br>
  <br>
  <button @click="setUserName()">获取reactive对象名字</button>


  <br>
  <br>
  {{color}}
  <br>
  <br>
<input type="text" v-model="color">

</template>


<script>
import { ref, reactive, toRefs } from 'vue'
export default {
  name: 'home',
  setup() {

    // 定义响应式

    // ref reactive 定义响应式数据
    let title = ref('我是一个标题')
    let animal = reactive({
      name: 'candy',
      color: 'white'
    })
    let userInfo = reactive({
      name: '邱诗梦',
      age: 24,
    })

    // 定义函数方法
    // 获取响应式数据
    let getUserName = () => {
      console.log(userInfo.name)
    }
    let getTitle = () => {
      console.log(title)
      console.log(title.value)
    }

    // 修改响应式数据
    let setUserName = () => {
      userInfo.name = 'qsm'
    }
    let setTitle = () => {
      title.value = '我是一个修改后的标题'
    }

    

    // 定义好的 响应式数据 和 函数方法 一定要 return 出去 统一出口
    return {
      // 响应式数据
      title,
      userInfo,
      // 方法
      getUserName,
      getTitle,
      setUserName,
      setTitle,
      ...toRefs(animal) // 结构reactive响应式数据
    }
  },
}
</script>

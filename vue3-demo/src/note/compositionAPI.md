<!--
 * @Author: lujiayu lujiayu@shiqiao.com
 * @Date: 2022-11-16 17:23:12
 * @LastEditors: lujiayu lujiayu@shiqiao.com
 * @LastEditTime: 2022-11-16 17:33:47
 * @FilePath: /vue3.0-test/vue3-demo/src/note/compositionAPI.vue
 * @Description: 这是默认设置,请设置`customMade`, 打开koroFileHeader查看配置 进行设置: https://github.com/OBKoro1/koro1FileHeader/wiki/%E9%85%8D%E7%BD%AE
-->

   # composition API 简介

    ** Options API **
    vue2中如何组织代码的：我们会在一个vue文件中data，methods，computed，watch中定义属性和方法，共同处理页面逻辑
    缺点： 一个功能往往需要在不同的vue配置项中定义属性和方法，比较分散，项目小还好，清晰明了，
          但是项目大了后，一个methods中可能包含很多个方法，往往分不清哪个方法对应着哪个功能
    优点：新手入门会比较简单

    ** Composition API **
    在vue3 Composition API 中，代码是根据逻辑功能来组织的，一个功能的所有api会放在一起（高内聚，低耦合），
    这样做，即时项目很大，功能很多，我们都能快速的定位到这个功能所用到的所有API，而不像vue2 Options API 
    中一个功能所用到的API都是分散的，需要改动，到处找API的过程是很费时间的
    缺点：学习成本可能会增加，以前的思维方式也要转变
    优点：Composition API 是根据逻辑相关性组织代码的，提高可读性和可维护性，基于函数组合的 API 
         更好的重用逻辑代码（在vue2 Options API中通过Mixins重用逻辑代码，容易发生命名冲突且关系不清）


    vue3.0 composition-api 可理解为 vue2.0中 data, computed, methods
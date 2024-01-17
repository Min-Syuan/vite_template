<template>
  <MainHeader/>
    


  <!-- 頁面路由route渲染的地方 -->
  <RouterView/>

  
  <!-- step2 -->
  <MainFooter 
    :content1="['dd', 'dd']"
    :content2="msg"
    @callParentPay="pay"
  />

  <MainFooter/>

  <MainFooter 
  v-for="item in 5"
  :content1="item"
  />



    

</template>

<script>
import { RouterLink, RouterView } from 'vue-router'
// import HelloWorld from '@/components/HelloWorld.vue'
import MainHeader from '@/components/MainHeader.vue'
import MainFooter from '@/components/MainFooter.vue'

export default {
  components: {
    // MainHead,
    // HelloWorld,
    RouterView,
    MainHeader,
    MainFooter,
  },
  data() {
    return {
      targetValue: 0,
      msg: 100,
      // msg: false
    }
  },
  created() {

  },
  methods: {
    // step3
    pay(money, str) {
      console.log('pay'+str)
      this.msg = this.msg + money
      // this.msg = !this.msg
    }
  },
};
</script>

<style scoped>
</style>
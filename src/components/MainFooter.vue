<template>
    <footer class="mainFooter">
      {{ content1 }}
      {{ content2 }}
      <input type="number" v-model="money">
      <Button @click="callMoney">我要錢</Button>
    </footer>
</template>

<script>
export default {
  data() {
    return {
      targetValue: 0,
      money: 0
    }
  },
  props:['content1', 'content2'],
  created() {},
  methods: {
    callMoney() {
      //step1:利用emit去呼叫父層
      // console.log('123')
      this.$emit('callParentPay', this.money, '嗨嗨')
    }
  },
}
</script>

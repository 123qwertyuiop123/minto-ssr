<template>
  <div class="app">
    <MtHeader class="mt-header"></MtHeader>
  </div>
</template>

<script>
import MtHeader from '../components/MtHeader.vue';
export default {
  name: 'IndexPage',
  components: {
    MtHeader
  },
  data() {
    return {
      a: 1
    }
  },
  //独立设置head信息
  head() {
    return {
      title: '成都明途科技有限公司-中国专业的目标大数据厂商',
      meta: [
        { name: 'description', content: '成都明途科技有限公司（MINTO）成立于2014年，总部设立于成都，专注于目标管理大数据领域，以互联网、大数据和人工智能技术为支撑，精心打造督查督办、目标绩效、重点项目等管理系统。' }
      ]
    }
  }
}
</script>
<style scoped>
.app {
  width: 100%;
}

.mt-header {
  position: fixed;
  top: 0;
}
</style>

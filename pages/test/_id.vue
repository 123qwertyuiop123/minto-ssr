<template>
  <div>
    <span>{{ test }}</span>
    <img :src="src" alt="" srcset="">
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: 'TestPage',
  data() {
    return {
      test: null,
      src: null
    }
  },
  mounted() {
    this.test = this.$route.params.id
    axios.get('https://api.thecatapi.com/v1/images/search?size=full').then(res => {
      this.src = res.data[0].url
    })
  },
  //独立设置head信息
  head() {
    return {
      title: this.test,
      meta: [
        { hid: 'description', name: 'news', content: 'tingqianyunluo' }
      ]
    }
  }
}
</script>

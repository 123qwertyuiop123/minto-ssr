<template>
  <div class="MtHeader">
    <img src="../assets/image/MtHeader/logo.webp" alt="" srcset="">
    <div v-for="(item, index) in menuList" :key="index" class="menu-item">
      {{ item.name }}
    </div>
    <div>{{ phone }}</div>
    <div class="btn">免费使用</div>
  </div>
</template>

<script>
export default {
  name: 'MtHeader',
  data() {
    return {

      menuList: [
        {
          name: '产品技术',
        },
        {
          name: '解决方案',
        },
        {
          name: '客户案例',
        },
        {
          name: '生态体系',
        },
        {
          name: '咨询动态',
        },
        {
          name: '关于明途',
        },
      ],
      phone: '400-001-0224/028-8562-52244'
    }
  }
}
</script>

<style lang="less" scoped>
.MtHeader {
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 20px 0;
}
.menu-item{
  padding: 0 25px;
}
.btn{

}
</style>

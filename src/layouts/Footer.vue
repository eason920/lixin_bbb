<template>
  <div class="footer">
     <a href="https://www.lixin.com.tw/" target="_blank"><img src="../assets/img/footerLogo.gif" alt="立炘數位" /></a>
     <a href="https://www.h35.tw/admin/test/login.php" target="_blank">網頁製作</a>
  </div>
</template>
<style lang="scss" scoped>
.footer {
  width: 100%;
  height: 40px;
  margin-bottom: 0px;
  background: #302626;
  display: flex;
  align-items: center;
  justify-content: center;

  img {
    width: 50px;
    margin-right: 20px;
  }

  p {
    font-size: 12px;
    color: rgba(255, 255, 255, 0.6);
    margin-right: 15px;
    margin-bottom: 0;
  }

  a {
    font-size: 12px;
    color: #fff;
    text-decoration: none;
  }
}

@media screen and (max-width: 767px) {
  .footer {
    margin-bottom: 63px;
  }
}

@media only screen and (max-width: 767px) {
  .footer {
    margin-bottom: 63px;
  }
}
</style>

<script>
export default {
  name: 'adminFooter',
  components: {},

  methods: {},
}
</script>

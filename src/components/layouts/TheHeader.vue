<template>
  <div class="navbar navbar-default topnav">
    <div class="container">
      <div class="navbar-header">
        <a href="/" class="navbar-brand">
          <span class="title">{{ logo.title }}</span>
          <img :src="logo.src" :alt="logo.title">
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TheHeader',
  data() {
    return {
      logo: {
        // src 的值是用反引号（`）标识的模板字符串，我们只需将变量放在 ${} 的大括号之中
        src: `${this.uploadsUrl}sites/ByvFbNlQYVwhvTyBgLdqitchoacDNznN.jpg`,
        title: 'VuejsCaff'
      }
    }
  },
  beforeCreate() {
    // 在当前实例上添加一个 uploadsUrl 属性
    this.uploadsUrl = 'https://vuejscaffcdn.phphub.org/uploads/'
  }
  // 由于用了 es6 语法，所以上边等价于
  // beforeCreate: function beforeCreate() {
  //   this.uploadsUrl = 'https://vuejscaffcdn.phphub.org/uploads/'
  // }
}
</script>

<style scoped>
.title { display: none;}
</style>

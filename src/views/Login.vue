<template>
  <div class="main">
    <div class="inputStyle">
      <div class="site">
        账号:<input type="text" v-model="username">
        密码:<input type="text" v-model="password">
        <button class="button" @click="sumbit">登录</button>
      </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  data() {
    return {
      username: '',
      password: ''
    }
  },
  methods: {
    sumbit() {
      axios.post("http://localhost:8080/user/login", {username: this.username, password: this.password})
          .then(res => {
            this.username = ''
            this.password = ''
            if (res.data.code == 200) {
              this.$router.push("/")
            } else {
              alert("账号或密码错误")
            }
          })
    },
    test() {
      axios.interceptors.request.use(config => {
        config.headers.token = 'eyJ0eXAiOiJKV1QiLCJhbGciOiJub25lIn0.eyJpZCI6MX0.' // 先使用假token进行测试
        return config
      }, error => {
        console.log(`err`, error)
      })
      axios.post("http://localhost:8080/user")
          .then(res => {
            console.log(res)
          })
    }
  }
}
</script>

<style scoped>
.main .inputStyle .site {
  height: 114px;
  width: 177px;
  margin: 0 0 0 0;
}

.main .button {
  width: 100px;
  height: 30px;
  background: rgba(33, 179, 46, 0.5);
}

.inputStyle {
  width: 244px;
  height: 114px;
  background: rgba(30, 211, 56, 0.5);
  padding: 43px 112px 43px 112px;
}

.main input {
  display: block;
}

.main {
  display: inline-block;
  margin: 200px 0 0 592px;
}
</style>

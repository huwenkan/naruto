<template>
  <div class="header">
    <div class="main">
      <ul>
        <li>
          <router-link to="/">
            主页
          </router-link>
        </li>
        <li>
          <router-link to="/memorandum">
            备忘录
          </router-link>
        </li>
        <li>
          <router-link to="/personal">
            个人中心
          </router-link>
        </li>
      </ul>
    </div>
    <div class="info">
      <ul>
        <li>
          <router-link to="/login">
            <span>登录</span>
          </router-link>
        </li>
        <li>
          <em>|</em>
        </li>
        <li>
          <router-link to="/register">
            <span>注册</span>
          </router-link>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {}
  }
}
</script>

<style scoped>
.header .info ul li {
  float: left;
}

.header .main ul li {
  float: left;
  margin-left: 50px;
}

.header .info em {
  font-style: normal;
}

.header .info {
  float: right;
  line-height: 60px;
}

.header .main {
  float: left;
  margin-left: 50px;
}

.header {
  line-height: 60px;
}

li {
  list-style: none;
  color: red;
}
</style>

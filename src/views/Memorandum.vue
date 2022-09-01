<template>
  <div class="main">
    <div class="site">
      <div class="input">
        <input>
        <button>添加</button>
      </div>
      <div class="table-site">
        <table>
          <!--          <tr v-for=""></tr>-->
        </table>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      msg: ''
    }
  },
  methods: {},
  mounted() {
  }
}
</script>

<style scoped>
.main .site .table-site {
  padding: 0 100px 0 100px;
}

.main .site .input button {
  float: left;
  height: 40px;
  width: 80px;
  margin-left: 10px;
  border-radius: 5px;
  border-color: aquamarine;
  box-shadow: 1px 1px 1px 1px black;
}
.main .site .input input{
  float: left;
  height: 39px;
  width: 400px;
  border: 1px black;
  border-radius: 5px;
  box-shadow: 1px 1px 1px 1px black;
}
.main .site .input {
  height: 40px;
  margin-left: 350px;
  margin-top: 10px;
}

.main .site {
  height: 1000px;
}

.main {
  display: inline-block;
  overflow: hidden;
  height: 940px;
  width: 1200px;
  background: rgba(30, 211, 56, 0.5);
  margin-left: 200px;
  border-radius: 10px;
}
</style>

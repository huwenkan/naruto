<template>
  <div>
    <form :action="avaterPath" method="post" enctype="multipart/form-data">
      头像上传：<input type="file" name="avater">
      <input type="submit" value="确认注册">
    </form>
    <div class="avater">
      <img src="../assets/img/gaodabeila.png" alt="">
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      avaterPath: 'http://localhost:8080/user/register'
    }
  }
}
</script>

<style scoped>
.avater img{
  height: 50px;
  width: 50px;
  border-radius: 50px;
  background: red;
}
</style>

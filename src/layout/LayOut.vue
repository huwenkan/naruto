<template>
  <div class="all">
    <div class="header">
      <Header class="Header"></Header>
    </div>
    <div class="main">
      <Main></Main>
    </div>
  </div>
</template>


<script>
import Header from "@/components/Header"
import Main from "@/components/Main"

export default {
  components: {
    Header,
    Main
  }
}

</script>

<style scoped>
.all .header .Header{
  padding: 0 400px;
}

.all .header {
  height: 60px;
}

.all {
  height: 1000px;
  /*background: url("../assets/img/gaodabeila.png") no-repeat fixed;*/
}
</style>

<template>
  <div class="line">
    <h1>Новый клиент</h1>
    <div class="all"></div>
  </div>
</template>

<script>
export default {
  name: 'Info',
  }
</script>

<style scoped>
h1{
  margin: 50px 0 40px 0;
  margin-left: 8%;
  margin-right: 8%;
}
.line{
    position: fixed;
    width: 20%;
    height: 800px;
    left: 5%;
    background-color: rgb(45, 92, 92);
    text-align: center;
    -webkit-box-shadow: 0px 0px 23px -5px rgba(0,0,0,0.75);
    -moz-box-shadow: 0px 0px 23px -5px rgba(0,0,0,0.75);
    box-shadow: 0px 0px 23px -5px rgba(0,0,0,0.75);
}
.all{
    width: 84%;
    min-height: 350px;
    height: fit-content;
    margin-left: 8%;
    border-radius: 10px;
    background-color: #fefffb;
    -webkit-box-shadow: inset 0px 0px 21px -5px rgba(0,0,0,0.75);
    -moz-box-shadow: inset 0px 0px 21px -5px rgba(0,0,0,0.75);
    box-shadow: inset 0px 0px 21px -5px rgba(0,0,0,0.75);
}
</style>
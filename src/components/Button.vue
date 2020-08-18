<template>
    <button >
        {{text}}
    </button>
</template>

<script>
export default {
  name: 'Button',
  props:{
      text: String,
  }
  }
</script>

<style scoped>
button{
    position: absolute;
    right: 37px;
    bottom: 24px;
    font-size: 18px;
    padding: 10px;
    border: none;
    border-radius: 5px;
    background-color: #fefffb;
    cursor: pointer;
    transition: all 200ms;
}
button:hover{
    border-radius: 20px;
}
button:focus{
  outline: none;
}
</style>
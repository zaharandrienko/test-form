<template>
  <div id="Form" v-bind:class="{element: anim}" :style="cssVars" v-on:click="anim = !anim">
    <h1>{{ form.title }}</h1>
    <div class="textInputs">
      <form>
        <strong>Фамилия</strong>
        <input class="textInput" type="text">
      </form>
            <form>
        <strong>Имя</strong>
        <input class="textInput" type="text">
      </form>
            <form>
        <strong>Отчество</strong>
        <input class="textInput" type="text">
      </form>
            <form>
        <strong>Дата рождения</strong>
        <input class="textInput" type="text">
      </form>
            <form>
        <strong>Номер телефона</strong>
        <input class="textInput" type="text">
      </form>
            <form>
        <strong>Пол</strong>
        <input class="textInput" type="text">
      </form>
      <form>
        <strong>Група клиентов</strong>
        <input class="textInput" type="text">
      </form>
      <form>
        <strong>Лечащий врач</strong>
        <input class="textInput" type="text">
      </form>
    </div>
    <label>
      <input type="checkbox" name="sms" value="yes" v-on:change="anim = !anim">Не отправлять СМС
    </label>
    <Button text="NEXT STEP >" :style="cssVars"/>
  </div>
</template>

<script>
import Button from '../components/Button.vue'

export default {
  name: 'Form',
  props: {
    form: {
      taype: Object,
      required: true,
    }
  },
  components: {
    Button
  },
  data(){
    return{
      anim: false
    }
  },
  computed: {
    cssVars() {
      return {
        '--bg-color': this.form.color,
        '--top': this.form.top + 'px',
        '--left': this.form.left + 'px'
      }
    }
  }
}
</script>

<style scoped>
h1 {
  margin: 10px;
  margin-bottom: 20px;
  font-size: 20px;
  margin-left: 20px;
}
#Form {
  position: absolute;
  width: 50%;
  height: 450px;
  top: var(--top);
  margin-left: var(--left);
  left: 35%;
  background-color: var(--bg-color);
  border-radius: 20px;
  -webkit-box-shadow: 5px 5px 23px -5px rgba(0,0,0,0.75);
  -moz-box-shadow: 5px 5px 23px -5px rgba(0,0,0,0.75);
  box-shadow: 5px 5px 23px -5px rgba(0,0,0,0.75);
}
.textInputs{
  width: 90%;
  margin-left: 5%;
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: 1fr 1fr;
  grid-column-gap: 20px;
  grid-row-gap: 20px;
}
strong{
  width: 100%;
  font-size: 20px;
}
.textInput{
  width: 100%;
  font-size: 18px;
  margin-top: 5px;
  border: none;
  border-radius: 5px;
  padding: 5px 0 5px 2px;
}
input:focus{
  outline: none;
  -webkit-box-shadow: inset 0px -61px 2px -56px rgb(143, 255, 143);
  -moz-box-shadow: inset 0px -61px 2px -56px rgba(143, 255, 143);
  box-shadow: inset 0px -61px 2px -56px rgba(143, 255, 143);

}
label{
  margin-left: 5%;
  width: 100%;
  font-size: 20px;
}
label input{
  margin-right: 10px;
  margin-top: 50px;
}
Button{
  color: var(--bg-color);
}
.element{
  z-index: -1;
  animation: animationFrames linear 4s;
  animation-iteration-count: 1;
  transform-origin: 50% 50%;
  -webkit-animation: animationFrames linear 4s;
  -webkit-animation-iteration-count: 1;
  -webkit-transform-origin: 50% 50%;
  -moz-animation: animationFrames linear 4s;
  -moz-animation-iteration-count: 1;
  -moz-transform-origin: 50% 50%;
  -o-animation: animationFrames linear 4s;
  -o-animation-iteration-count: 1;
  -o-transform-origin: 50% 50%;
  -ms-animation: animationFrames linear 4s;
  -ms-animation-iteration-count: 1;
  -ms-transform-origin: 50% 50%;
}

@keyframes animationFrames{
  0% {
    transform:  translate(0px,0px)  ;
  }
  7% {
    transform:  translate(-1700px,-43px)  ;
  }
  13% {
    transform:  translate(80px,-80px)  ;
  }
  100% {
    transform:  translate(80px,-80px)  ;
  }
}

@-moz-keyframes animationFrames{
  0% {
    -moz-transform:  translate(0px,0px)  ;
  }
  7% {
    -moz-transform:  translate(-1700px,-43px)  ;
  }
  13% {
    -moz-transform:  translate(80px,-80px)  ;
  }
  100% {
    -moz-transform:  translate(80px,-80px)  ;
  }
}

@-webkit-keyframes animationFrames {
  0% {
    -webkit-transform:  translate(0px,0px)  ;
  }
  7% {
    -webkit-transform:  translate(-1700px,-43px)  ;
  }
  13% {
    -webkit-transform:  translate(80px,-80px)  ;
  }
  100% {
    -webkit-transform:  translate(80px,-80px)  ;
  }
}

@-o-keyframes animationFrames {
  0% {
    -o-transform:  translate(0px,0px)  ;
  }
  7% {
    -o-transform:  translate(-1700px,-43px)  ;
  }
  13% {
    -o-transform:  translate(80px,-80px)  ;
  }
  100% {
    -o-transform:  translate(80px,-80px)  ;
  }
}

@-ms-keyframes animationFrames {
  0% {
    -ms-transform:  translate(0px,0px)  ;
  }
  7% {
    -ms-transform:  translate(-1700px,-43px)  ;
  }
  13% {
    -ms-transform:  translate(80px,-80px)  ;
  }
  100% {
    -ms-transform:  translate(80px,-80px)  ;
  }
}
</style>

<template>
  <div class="big-title" id="Main" style="position: relative;">
      <div style="position: absolute; left: 50%; top: 50%;">
      <Trigger @triggerShow="$emit('show')"/>
      </div>
      <b-container class="big-title-center">
          <b-row><LogoHse class="title-hse"/></b-row>
          <b-row><TitleLabel class="title-label"/></b-row>
          <b-row><LogoSponsor class="title-sponsors"/></b-row>
      </b-container>
  </div>
</template>
<script>
import Trigger from './Trigger';
export default {

}
</script>
<style>
.big-title {
  width: 100vw;
}
.big-title-center {
  display: flex;
  justify-content: flex-end;
  align-items: center;
  flex-wrap: wrap;
  width: 80%;
  padding: 30px;
}
.title-label {
  margin: 23px 0 23px 0
}
@media only screen and (min-device-width: 770px) {
  .title-label {
     width: 616px;
     height: 555px;
  }
  .title-sponsors {
    width: 616px;
  }
  .title-hse {
    width: 616px;
  }
  .big-title {
    background: url('~assets/background.gif') no-repeat center/100% 100%;
  }
}
@media only screen and (max-width: 770px) {
  .big-title {
    background: url('~assets/joystick.png') no-repeat center/cover,
                url('~assets/background.png') no-repeat center/100% 100%;
  }
}
</style>

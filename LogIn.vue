<template>
  <view class="container">
    <image-background :source="login" class="login">
      <image class="logo"
      :style="{width: 400, height: 200, alignContent: 'center'}"
      :source="{uri: '/Users/debroniswarren/playground2/stem-city-front/assets/images/imageedit_1_2155572343.png'}"
    ></image>
    <text class="title">Log In</text>
    <view class="input-container">
      <text-input class="input" auto-capitalize="none" v-model="firstName" placeholder="First Name"/>
      <text-input class="input" auto-capitalize="none"  v-model="lastName" placeholder="Last Name"/>
      <text-input class="input" auto-capitalize="none"  v-model="email" placeholder="Email"/>
    </view>
  </view>
</template>
<script>
import login from "/Users/debroniswarren/playground2/stem-city-front/assets/images/photo-1517009572053-93fb56dfef49.jpeg";
export default {
  props: {
    navigation: {
      type: Object
    }
  },
  data() {
    return {
      message: "",
      myInput: "",
      firstName: "",
      lastName: "",
      email: "",
      login: login
      
    };
  }
};
</script>
<style>
.container {
  
  align-items: center;
  justify-content: flex-start;
  flex: 1;
}
.input {
  height: 50;
  width: 300;
  border-radius: 10;
  border-color: gray;
  border-width: 1;
  align-content: center;
  
}
.input-container {
    display:flex;
    align-content: center;
    justify-content: space-evenly;
    height: 300;
    width: 300;
}
.login {
  flex: 1;
  width: 100%;
}
</style>
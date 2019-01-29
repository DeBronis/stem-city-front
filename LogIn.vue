<template>
  <view class="container">
    <image-background :source="login" class="login">
      <image :source="logo" class="logo"></image>
    <text class="title">Log In</text>
    <view class="input-container">
      <text-input class="input" auto-capitalize="none" v-model="firstName" placeholder="First Name"/>
      <text-input class="input" auto-capitalize="none"  v-model="lastName" placeholder="Last Name"/>
      <text-input class="input" auto-capitalize="none"  v-model="email" placeholder="Email"/>
      <text-input class="input" auto-capitalize="none"  v-model="password" placeholder="Password"/>
    </view>
    <view>
      <touchable-opacity  class="button2" :on-press="handleSignUp"
      :style="{padding: 10}">
       <text class="button-text">Submit</text>
    </touchable-opacity>
    </view>
  </view>
</template>
<script>
import login from "/Users/debroniswarren/playground2/stem-city-front/assets/images/photo-1501769214405-5e5ee5125a02.jpeg";
import logo from "/Users/debroniswarren/playground2/stem-city-front/assets/images/imageedit_1_2155572343.png";
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
      password: "",
      login: login,
      logo: logo
      
    };
  },
  methods:{
    handleSignUp() {
      this.navigation.navigate("Map"); 
    }
  }
};
</script>
<style>
.container {
  flex: 1;
  display: flex;
  justify-content: center;
  align-items: center;
  align-content: center;
}
.input {
  height: 50;
  width: 300;
  border-radius: 10;
  border-color: black;
  border-width: 1;
  align-content: center;
  font-family: Courier;
  font-size: 25;
  color:black;
  
}
.input-container {
  height: 250;
  width: 150;
  display: flex;
  justify-content: space-evenly;
  position: relative; left: 15%; bottom: -8%;
  /* opacity: .50; */ 
}
.login {
  flex: 1;
  width: 100%;
}
.logo {
  width: 90%;
  height: 27%;
  position: relative; left: 5%; 
    
}
.button2 {
   height: 100;
  width: 150;
  background-color: azure;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 10;
  border-width: 2;
  align-content: center;
  opacity: .50;
  position: relative; left: 30%; bottom: -80%;
}
.title {
  font-family: Courier;
  font-size: 25;
  color:black;
  position: relative; left: 35%;
}
</style>
<template>
  <view class="container">
  <image-background :source="home" class="home">
    <image :source="logo" class="logo"
    ></image>
    <view class="container2">
    <touchable-opacity class="button1" :on-press="handleLogIn"
      :style="{padding: 10}">
      
      <text class="button-text">Log In</text>
	    

    </touchable-opacity>
    <touchable-opacity  class="button2" :on-press="handleSignUp"
      :style="{padding: 10}">
       <text class="button-text">Sign-Up</text>
	    

    </touchable-opacity>
    </view>
    </view>
</template>

<script>
import React from 'react'
import {Text} from 'react-native'
import home from "/Users/debroniswarren/playground2/stem-city-front/assets/images/photo-1517009572053-93fb56dfef49.jpeg";
import logo from "/Users/debroniswarren/playground2/stem-city-front/assets/images/imageedit_1_2155572343.png";
export default {
    props: {
        navigation: {
            type: Object
        }
    },
  data() {
    return {
      message: "Hello, world!",
      myInput: "",
      home: home,
      logo: logo
    };
  },
  methods:{
    handleSignUp() {
      this.navigation.navigate("SignUp"); 
    },
    handleLogIn() {
      this.navigation.navigate("LogIn"); 
    }
    // renderList: function(item) {
    //     return (<Text>{item.item.key}</Text>)
    // }
  }
};
</script>

<style>
.container {
  
  /* align-items: center;
  justify-content: flex-start; */
  flex: 1;
  display: flex;
  justify-content: center;
  align-items: center;
  align-content: center;
  
}
.container2 {
  height: 250;
  width: 150;
  display: flex;
  justify-content: space-evenly;
  position: relative; left: 30%; top: 20%;
}
.text-color-primary {
  color: blue;
  font-size: 20;
}
.logo {
  width: 90%;
  height: 27%;
  position: relative; left: 5%; 
  color: transparent;
  
}
.home {
  flex: 1;
  width: 100%;
}
.button1 {
  height: 100;
  width: 150;
  background-color: transparent;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 10;
  border-width: 2;
}
.button2 {
   height: 100;
  width: 150;
  background-color: transparent;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 10;
  border-width: 2;
  align-content: center;
  
}
.button-text {
  font-family: Courier;
  font-size: 25;
  color:black;
  
}

</style>

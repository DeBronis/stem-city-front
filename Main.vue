<template>
  <view class="container">
    <!-- <text class="text-color-primary">S.T.E.M. City</text> -->
    <!-- <text>{{ myInput }}</text> -->
    <image class="background"
      :style="{width: 400, height: 300}"
      :source="{uri: 'https://i.ibb.co/LtgPmYz/Screen-Shot-2019-01-23-at-12-58-53-PM.png'}"
    ></image>

    <touchable-opacity 
      :on-press="handleLogIn"
      :style="{padding: 10}"
      >
      <text style="{ color: 'white'}">Log In</text>
    </touchable-opacity>
    <touchable-opacity 
      :on-press="handleSignUp"
      :style="{padding: 10}"
      >
      <text style="{ color: 'white'}">Sign Up</text>
    </touchable-opacity>
    <!-- <button
        :on-press="handleButton"
        title="My Button"
        color="#841584"
        accessibility-label="Learn more about this purple button"
    /> -->
    <!-- <flat-list
        :data="[{key: 'a'}, {key: 'b'}]"
        :render-item="(item) => renderList(item)"
    /> -->
  
  </view>
</template>

<script>
// import React from 'react'
// import {Text} from 'react-native'
export default {
    props: {
        navigation: {
            type: Object
        }
    },
  data() {
    return {
      message: "Hello, world!",
      myInput: ""
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
  background-color: white;
  align-items: center;
  justify-content: flex-start;
  flex: 1;
}
.text-color-primary {
  color: blue;
  font-size: 20;
}
.background {
    color: transparent;
    align-items: center;
  justify-content: flex-start;
}

</style>

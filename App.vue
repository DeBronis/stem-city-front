<template>
  <view class="container">
    <text class="text-color-primary">S.T.E.M. City</text>
    <text>{{ myInput }}</text>
    <image class="background"
      :style="{width: 300, height: 300}"
      :source="{uri: 'https://assets.visitphilly.com/wp-content/uploads/2016/09/Philadelphia_Skyline_from_Loews_Hotel_SPLxpuHFN6-ouNEZSqecsTs18q0ABlZBh_rgb_72-924x693.jpg'}"
    ></image>
    <text-input
      :style="{height: 40, width: 350, borderColor: 'gray', borderWidth: 1}"
      v-model="myInput"
    />
    <touchable-opacity 
      :on-press="handleButton"
      :style="{backgroundColor: 'red', padding: 10}"
      >
      <text style="{ color: 'white'}">My Button</text>
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
  data() {
    return {
      message: "Hello, world!",
      myInput: ""
    };
  },
  methods:{
    handleButton() {
      this.myInput = 'Button clicked'
    },
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
  justify-content: center;
  flex: 1;
}
.text-color-primary {
  color: blue;
  font-size: 20;
}

</style>

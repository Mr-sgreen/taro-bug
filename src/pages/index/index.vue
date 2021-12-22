<template>
  <view class="index">
    <text>{{ msg }}</text>
  </view>
</template>

<script>
import { ref } from 'vue'
import './index.scss'
import Taro from '@tarojs/taro';

export default {
  setup() {
    const msg = ref('Hello world')
    Taro.showModal({
      title: '温馨提示',
      content: '记得按时吃饭',
      showCancel: false,
      confirmColor: '#276FF5',
      confirmText: '知道了',
    });
    return {
      msg
    }
  }
}
</script>

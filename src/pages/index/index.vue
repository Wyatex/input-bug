<template>
  <view class="demo">
    <view> 欢迎使用 NutUI 开发 Taro 多端项目 <Dongdong /> </view>
    <view>
      <nut-input v-model="word" @confirm="handleConfirm('confirm')" />
      <nut-button @click="handleConfirm('click')">确定</nut-button>
    </view>
    <view>
      {{ word }}
    </view>
  </view>
</template>

<script setup>
import { ref } from 'vue'
import { Dongdong } from '@nutui/icons-vue-taro'

const word = ref()

const handleConfirm = (from) => {
  console.log(from)
  word.value = ''
}
</script>

<style>
.demo {
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
</style>

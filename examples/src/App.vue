<script setup lang="ts">
import Mobile from '../../docs/.vitepress/theme/Mobile/index.vue'
import { BeeMessage } from '@bee-ui/components'

const handleShowMessage = (type: any) => {
  BeeMessage({
    type,
    message: '你妈妈买的你妈妈买的你妈妈买的你妈妈买的你妈妈买的',
    duration: 1000 * 1000,
    icon: 'sousuo',
    onClose: () => false,
    customClass: "日你吗的·"
  })
}
</script>

<template>
  <div style="display: flex; align-items: center; width: 100vw; height: 100vh; background-color: #8b8b8b">
    <Mobile>
      <BeeButton @click="handleShowMessage('success')" circle inline style="margin-bottom: 10px">success</BeeButton>
      <BeeButton @click="handleShowMessage('error')" circle inline style="margin-bottom: 10px">error</BeeButton>
      <BeeButton @click="handleShowMessage('warning')" circle inline style="margin-bottom: 10px">warning</BeeButton>
      <BeeButton @click="handleShowMessage('info')" circle inline style="margin-bottom: 10px">info</BeeButton>

      <!-- <div style="box-sizing: border-box; margin: 10px">
        <BeeButton @click="handleShowMessage" circle inline style="margin-bottom: 10px">文</BeeButton>
        <BeeButton circle icon="sousuo" size="mini" inline style="margin-bottom: 10px" type="primary"></BeeButton>
        <BeeButton circle loading size="small" inline style="margin-bottom: 10px" type="success"></BeeButton>
        <BeeButton icon="message" circle size="large" inline style="margin-bottom: 10px" type="info"></BeeButton>
      </div>

      <hr />
      <div style="box-sizing: border-box; margin: 10px">
        <BeeButton inline style="margin-bottom: 10px">default</BeeButton>
        <BeeButton size="mini" inline style="margin-bottom: 10px" type="primary">primary</BeeButton>
        <BeeButton loading size="small" inline style="margin-bottom: 10px" type="success">success</BeeButton>
        <BeeButton icon="sousuo" size="large" inline style="margin-bottom: 10px" type="info">info</BeeButton>
        <BeeButton inline style="margin-bottom: 10px" type="warning">warning</BeeButton>
        <BeeButton inline style="margin-bottom: 10px" type="danger">danger</BeeButton>
        <BeeButton icon="sousuo" inline style="margin-bottom: 10px" type="text">text</BeeButton>
      </div>

      <hr />
      <div style="box-sizing: border-box; margin: 10px">
        <BeeButton icon="sousuo" style="margin-bottom: 10px" type="primary">primary</BeeButton>
        <BeeButton loading icon="sousuo" style="margin-bottom: 10px" type="primary">primary</BeeButton>
        <BeeButton icon-position="left" icon="message" round style="margin-bottom: 10px">default</BeeButton>
        <BeeButton loading icon-position="left" icon="message" round style="margin-bottom: 10px">default</BeeButton>
      </div>

      <hr />

      <div style="box-sizing: border-box; margin: 10px">
        <BeeButton bg="#f00" round style="margin-bottom: 10px" type="primary">primary</BeeButton>
        <BeeButton disabled bg="#098" round color="#333" style="margin-bottom: 10px">default</BeeButton>
      </div>

      <hr />

      <div style="box-sizing: border-box; margin: 10px">
        <BeeButton disabled round style="margin-bottom: 10px">default</BeeButton>
        <BeeButton disabled round style="margin-bottom: 10px" type="primary">primary</BeeButton>
        <BeeButton disabled round style="margin-bottom: 10px" type="success">success</BeeButton>
        <BeeButton disabled round style="margin-bottom: 10px" type="info">info</BeeButton>
        <BeeButton disabled round style="margin-bottom: 10px" type="warning">warning</BeeButton>
        <BeeButton disabled round style="margin-bottom: 10px" type="danger">danger</BeeButton>
        <BeeButton disabled round style="margin-bottom: 10px" type="text">text</BeeButton>
      </div>

      <hr />
      <div style="box-sizing: border-box; margin: 10px">
        <BeeButton color="#543" style="margin-bottom: 10px" type="primary">custorm</BeeButton>
        <BeeButton color="#f40" plain style="margin-bottom: 10px" type="primary">custorm</BeeButton>
        <BeeButton disabled color="#789" style="margin-bottom: 10px" type="primary">custorm</BeeButton>
      </div>

      <hr />
      <div style="box-sizing: border-box; margin: 10px">
        <BeeButton round style="margin-bottom: 10px">default</BeeButton>
        <BeeButton round style="margin-bottom: 10px" type="primary">primary</BeeButton>
        <BeeButton round style="margin-bottom: 10px" type="success">success</BeeButton>
        <BeeButton round style="margin-bottom: 10px" type="info">info</BeeButton>
        <BeeButton round style="margin-bottom: 10px" type="warning">warning</BeeButton>
        <BeeButton round style="margin-bottom: 10px" type="danger">danger</BeeButton>
        <BeeButton round style="margin-bottom: 10px" type="text">text</BeeButton>
      </div>

      <hr />
      <div style="box-sizing: border-box; margin: 10px">
        <BeeButton plain style="margin-bottom: 10px">default</BeeButton>
        <BeeButton plain style="margin-bottom: 10px" type="primary">primary</BeeButton>
        <BeeButton plain style="margin-bottom: 10px" type="success">success</BeeButton>
        <BeeButton plain style="margin-bottom: 10px" type="info">info</BeeButton>
        <BeeButton plain style="margin-bottom: 10px" type="warning">warning</BeeButton>
        <BeeButton plain style="margin-bottom: 10px" type="danger">danger</BeeButton>
        <BeeButton plain style="margin-bottom: 10px" type="text">text</BeeButton>
      </div>

      <hr />
      <div style="box-sizing: border-box; margin: 10px">
        <BeeButton size="mini" style="margin-bottom: 10px">mini</BeeButton>
        <BeeButton size="small" style="margin-bottom: 10px" type="primary">small</BeeButton>
        <BeeButton size="" style="margin-bottom: 10px" type="success">normal</BeeButton>
        <BeeButton size="large" style="margin-bottom: 10px" type="info">large</BeeButton>
      </div>

      <hr />

      <div style="padding: 0 10px; box-sizing: border-box; margin: 10px 0">
        <BeeButton style="margin-bottom: 10px">default</BeeButton>
        <BeeButton style="margin-bottom: 10px" type="primary">primary</BeeButton>
        <BeeButton style="margin-bottom: 10px" type="success">success</BeeButton>
        <BeeButton style="margin-bottom: 10px" type="info">info</BeeButton>
        <BeeButton style="margin-bottom: 10px" type="warning">warning</BeeButton>
        <BeeButton style="margin-bottom: 10px" type="danger">danger</BeeButton>
        <BeeButton style="margin-bottom: 10px" type="text">text</BeeButton>
      </div> -->
    </Mobile>
  </div>
</template>

<style scoped></style>

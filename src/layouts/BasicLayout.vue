<script setup lang="ts">
import GlobalHeader from "@/components/GlobalHeader.vue";
</script>

<template>
<div id="basic-layout">
  <a-layout style="min-height: 100vh">
    <a-layout-header>
      <GlobalHeader/>
    </a-layout-header>
    <a-layout-content>
      <router-view/>
    </a-layout-content>
    <a-layout-footer>
      <a href="https://www.google.com" target="_blank">Google</a>

    </a-layout-footer>
  </a-layout>
</div>
</template>

<style scoped>
#basic-layout .ant-layout-header {
  padding-inline: 20px;
  margin-bottom: 16px;
  color: unset;
  background: #fff;
}

#basic-layout .ant-layout-content{
  background: purple;
  margin-bottom: 28px;
  padding: 20px;
}

#basic-layout .ant-layout-footer{
  display: flex;
  height: 100px;
  width: 100%;
  align-items: center;
  justify-content: center;
  padding: 16px;
  background: #efefef;
  position: fixed;
  bottom: 0;
  text-align: center;
}
</style>
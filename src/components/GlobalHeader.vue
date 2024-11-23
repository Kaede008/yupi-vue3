<template>
  <div id="global-header">
    <a-row :wrap="false">
      <a-col flex="200px">
        <div class="title-bar">
          <img class="logo" src="../assets/logo.webp" alt="logo">
          <div class="title">鱼皮用户中心</div>
        </div>
      </a-col>
      <a-col flex="auto">
        <a-menu v-model:selectedKeys="current" mode="horizontal" :items="items" />
      </a-col>
      <a-col flex="80px">
        <div class="user-login-status">
          <a-button type="primary" href="/user/login">登录</a-button>
        </div>
      </a-col>
    </a-row>

  </div>
</template>
<script setup>
import { h, ref } from 'vue';
import { SettingOutlined, HomeOutlined } from '@ant-design/icons-vue';
const current = ref(['mail']);
const items = ref([
  {
    key: '/',
    icon: () => h(HomeOutlined),
    label: '主页',
    title: '主页',
  },
  {
    key: '/user/login',
    label: '用户登录',
    title: '用户登录',
  },
  {
    key: '/user/register',
    label: '用户注册',
    title: '用户注册',
  },
  {
    key: '/admin/manage',
    icon: () => h(SettingOutlined),
    label: "用户管理",
    title: '用户管理',
  },
  {
    key: "others",
    label: h(
        "a",
        {href:"https://www.google.com", target:"_blank"},
        "Google"
    ),
    title: "Google",
  },
]);
</script>

<style scoped>
.title-bar {
  display: flex;
  align-items: center;
}

.title {
  color: #000;
  font-size: 18px;
  margin-left: 16px;
}

.logo {
  height: 48px;
}

</style>
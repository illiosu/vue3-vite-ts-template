<template>
  <el-button type="primary" size="small" icon="Refresh" circle @click="updateRefresh"></el-button>
  <el-button type="primary" size="small" icon="FullScreen" circle></el-button>
  <el-button type="primary" size="small" icon="Setting" circle></el-button>
  <img src="/logo.png" style="width: 24px; height: 24px; margin: 0px, 10px" />
  <!-- 下拉菜单 -->
  <el-dropdown>
    <span class="el-dropdown-link">
      admin
      <el-icon class="el-icon--right">
        <arrow-down />
      </el-icon>
    </span>
    <template #dropdown>
      <el-dropdown-menu>
        <el-dropdown-item>退出登录</el-dropdown-item>
      </el-dropdown-menu>
    </template>
  </el-dropdown>
</template>

<script setup lang="ts">
import useLayOutSettingStore from '@/store/modules/setting';
let layOutSettingStore = useLayOutSettingStore();

//刷新按钮点击回调
const updateRefresh = () => {
  layOutSettingStore.refresh = !layOutSettingStore.refresh;
};
</script>
<style lang="scss" scoped></style>

<template>
  <div class="tabbar">
    <div class="tabbar-left">
      <Breadcrumb></Breadcrumb>
    </div>
    <div class="tabbar-right">
      <Setting></Setting>
    </div>
  </div>

  <!-- <el-breadcrumb separator-icon="ArrowRight">
    <el-breadcrumb-item v-for="(item, index) in $route.matched" :key="index" v-show="item.meta.title" :to="item.path">
      <el-icon>
        <component :is="item.meta.icon"></component>
      </el-icon>
    </el-breadcrumb-item>
  </el-breadcrumb> -->
</template>
<script setup lang="ts">
import useLayOutSettingStore from '@/store/modules/setting';
import Breadcrumb from './breadcrumb/index.vue';
import Setting from './setting/index.vue';

</script>
<script lang="ts">
export default {
  name: 'Breadcrumb',
};
</script>
<style scoped lang="scss">
.tabbar {
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: space-between;
  //渐变色，先不加
  // background-image: linear-gradient(to right, #f5f5f5, #363434);
  .tabbar-left {
    display: flex;
    align-items: center;
    margin-left: 20px;
  }
  .tabbar-right {
    display: flex;
    align-items: center;
    // margin-right: 20px;
  }
}
</style>

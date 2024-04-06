<template>
  <div class="logo" v-if="!setting.logoHidden">
    <img :src="setting.logo" alt="" />
    <p v-show="!LayOutSettingStore.fold">{{ setting.title }}</p>
  </div>
</template>
<style lang="scss" scoped>
.logo {
  color: white;
  display: flex;
  align-items: center;
  padding: 20px;

  img {
    width: $base-slider-min-width;
    height: $base-slider-logo-height;

    // width: if( LatOutSettingStore , cyan, green);
  }

  p {
    font-size: $base-logo-title-fontSize;
    margin-left: 10px;
  }
}
</style>
<script setup lang="ts">
import setting from '@/setting';
import useLayOutSettingStore from '@/store/modules/setting';
let LayOutSettingStore = useLayOutSettingStore();
console.log(LayOutSettingStore.fold);
</script>

<template>
  <div id="app">
    <drawer :show-mode="drawerConfig.mode"
            :placement="drawerConfig.placement"
            :drawer-style="drawerConfig.style">
      <div slot="drawer">
      <!-- 菜单内容 -->
      </div>
      <div>
        <router-view></router-view>
      </div>
    </drawer>
    <tabbar>
      <tabbar-item>
        <span slot="label">Wechat</span>
      </tabbar-item>
      <tabbar-item>
        <span slot="label">Message</span>
      </tabbar-item>
    </tabbar>
  </div>
</template>

<script>
import { Drawer, Tabbar } from 'vux'

export default {
  name: 'App',
  components: {
    Drawer,
    Tabbar
  },
  data: () => ({
    drawerConfig: {
        mode: 'overlay',
        placement: 'left',
        style: {
          width: '200px',
          backgroundColor: '#35495e'
        }
      },
  })
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

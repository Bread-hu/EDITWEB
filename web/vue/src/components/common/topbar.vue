<template>
  <div style="text-align: center;margin: 0 auto">
    <el-menu
      default-active="activeIndex"
      class="el-menu-demo"
      mode="horizontal"
      style="display: inline-block;width: 40%;vertical-align:middle;border: none"
    >
      <el-menu-item
        v-for="item in button_list"
        :key="item.name"
        index="item.name"
        @click="goPage(item.path)"
        style="font-size: 20px"
      >{{ item.name }}
      </el-menu-item
      >
    </el-menu>
  </div>
</template>

<script>
export default {
  name: 'topbar',
  data() {
    return {

      button_list: [
        {name: "首页", path: "/"},
        {name: "笔记", path: "/"},
        {name: "待定", path: '/'},
        {name: '待定', path: '/'},
      ]
    }
  },
  methods: {
    goPage (path) {
      this.$router.push(path)
    }
  }
}
</script>

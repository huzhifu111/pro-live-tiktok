<template>
  <div class="tab-bar">
    <div class="item" @click="changeTab(0)">
      <router-link to="/index" tag="span" :class="tabIndex==0?'active':''">首页</router-link>
    </div>
    <div class="item" @click="changeTab(1)">
      <router-link to="/friends" tag="span" :class="tabIndex==1?'active':''">朋友</router-link>
    </div>
    <div class="item" @click="changeTab(2)">
      <router-link to="/index" tag="span" :class="tabIndex==2?'active':''">+</router-link>
    </div>
    <div class="item" @click="changeTab(3)">
      <router-link to="/message" tag="span" :class="tabIndex==3?'active':''">消息</router-link>
    </div>
    <div class="item" @click="changeTab(4)">
      <router-link to="/account" tag="span" :class="tabIndex==4?'active':''">我</router-link>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      tabIndex: 0,
    };
  },

  methods: {
    changeTab: function (e) {
      this.tabIndex = e;
    },
  },
};
</script>

<style scoped>
.tab-bar {
  height: 50px;
  line-height: 50px;
  width: 100%;
  background: #000;
  position: fixed;
  bottom: 0;
  left: 0;
  color: #cccccc;
  font-size: 16px;
  display: flex;
  justify-items: center;
}

.tab-bar .item {
  flex: 1;
  text-align: center;
}

.tab-bar .item .active {
  color: #fff;
}

.tab-bar .item .dy-btn {
  width: 50px;
  height: 30px;
  padding: 1px;
}
</style>
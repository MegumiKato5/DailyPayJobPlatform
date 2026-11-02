<template>
  <view class="wrap" style="background:#1c1c1e;padding-bottom:100rpx;">
    <!-- 顶部标题 -->
    <view class="header">
      <view class="title">消息</view>
    </view>

    <!-- 标签栏：沟通 / 通知 -->
    <view class="tab-nav">
      <view class="nav-item active">沟通</view>
      <view class="nav-item">通知</view>
    </view>

    <!-- 聊天列表 -->
    <view class="chat-list">
      <view class="chat-item" v-for="(item,idx) in ChatList" :key="idx">
        <image :src="item.image" mode="aspectFill" class="avatar"></image>
        <view class="chat-main">
          <view class="row-top">
            <view class="chat-name">{{item.chatname}}</view>
            <view class="time">{{item.time}}</view>
          </view>
          <view class="row-bottom">
            <view class="last-msg">{{item.lastmsg}}</view>
            <view class="badge" v-show="item.badge>=1">{{item.badge}}</view>
          </view>
        </view>
      </view>

   
    </view>
  </view>
</template>

<script setup>
	const ChatList=[
		//测试
		{id:0,chatname:'前端岗位负责人',time:"昨天",lastmsg:"简历收到了，稍后给你回复",image:"/static/SelectineMine.png",badge:1},
		{id:1,chatname:'原神岗位负责人',time:"10:12",lastmsg:"简历收到了，稍后给你回复",image:"/static/SelectineMine.png",badge:0},
	]
	
</script>

<style scoped>
.wrap {
  min-height: 100vh;
  padding-bottom:100rpx
}
.header {
  background: #2c2c2e;
  padding: 30rpx;
}
.title {
  font-size: 36rpx;
  font-weight: bold;
  color: #fff;
}
.tab-nav {
  display: flex;
  background: #2c2c2e;
  border-bottom: 1rpx solid #444;
}
.nav-item {
  flex: 1;
  text-align: center;
  padding: 24rpx 0;
  font-size: 28rpx;
  color: #aaa;
}
.nav-item.active {
  color: #0088cc;
  font-weight: bold;
  position: relative;
}
.nav-item.active::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 50%;
  transform: translateX(-50%);
  width: 60rpx;
  height: 4rpx;
  background: #0088cc;
  border-radius: 2rpx;
}
.chat-list {
  margin-top: 20rpx;
  background: #2c2c2e;
}
.chat-item {
  display: flex;
  align-items: center;
  padding: 24rpx;
  border-bottom: 1rpx solid #444;
  gap: 20rpx;
}
.avatar {
  width: 96rpx;
  height: 96rpx;
  border-radius: 50%;
}
.chat-main {
  flex: 1;
  overflow: hidden;
}
.row-top {
  display: flex;
  justify-content: space-between;
  margin-bottom: 8rpx;
}
.chat-name {
  font-size: 30rpx;
  color: #fff;
}
.time {
  font-size: 24rpx;
  color: #999;
}
.row-bottom {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.last-msg {
  font-size: 26rpx;
  color: #aaa;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  flex: 1;
  margin-right: 12rpx;
}
.badge {
  background: #f56c6c;
  color: #fff;
  font-size: 20rpx;
  padding: 2rpx 10rpx;
  border-radius: 20rpx;
  min-width: 32rpx;
  text-align: center;
}
</style>
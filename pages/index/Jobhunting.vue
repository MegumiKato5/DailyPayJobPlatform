<template>
  <view class="wrap" style="background:#1c1c1e;padding-bottom:60rpx;">
    <!-- 顶部个人信息卡片 -->
    <view class="card">
      <view class="user-header">
        <uni-icons type="person" size="128" color="#888"><image src="/static/SelectineMine.png" mode="aspectFill" class="avatar-img"></image></uni-icons>
        <view class="user-info">
          <view class="name">求职者</view>
          <view class="tip">求职状态：在职-看机会</view>
        </view>
        <uni-icons type="settings" size="44" color="#fff" style="margin-left:auto;"></uni-icons>
      </view>
      <view class="data-row">
        <view class="data-item">
          <view class="num">2862</view>
          <view class="label">沟通</view>
        </view>
        <view class="data-item">
          <view class="num">12</view>
          <view class="label">面试</view>
        </view>
        <view class="data-item">
          <view class="num">45</view>
          <view class="label">已读</view>
        </view>
        <view class="data-item">
          <view class="num">108</view>
          <view class="label">邀约</view>
        </view>
      </view>
    </view>

    <!-- 常用功能 -->
    <view class="card">
      <view class="card-title">常用功能</view>
      <view class="grid-row">
        <view class="func-item">
          <uni-icons type="document" size="48" color="#fff"></uni-icons>
          <text>在线简历</text>
        </view>
        <view class="func-item">
          <uni-icons type="paperclip" size="48" color="#fff"></uni-icons>
          <text>附件简历</text>
        </view>
        <view class="func-item">
          <uni-icons type="target" size="48" color="#fff"></uni-icons>
          <text>求职意向</text>
        </view>
        <view class="func-item">
          <uni-icons type="gear" size="48" color="#fff"></uni-icons>
          <text>求职工具</text>
        </view>
      </view>
    </view>

    <!-- 其他功能列表 -->
    <view class="card">
      <view class="card-title">其他功能</view>
      <view class="list-item">
        <uni-icons type="heart" size="40" color="#fff"></uni-icons>
        <text>关注公司</text>
      </view>
      <view class="list-item">
        <uni-icons type="star" size="40" color="#fff"></uni-icons>
        <text>收藏职位</text>
      </view>
      <view class="list-item">
        <uni-icons type="clock" size="40" color="#fff"></uni-icons>
        <text>浏览记录</text>
      </view>
      <view class="list-item">
        <uni-icons type="help" size="40" color="#fff"></uni-icons>
        <text>帮助与反馈</text>
      </view>
    </view>

    <!-- 底部模拟tab（如果你不用pages.json原生tabbar就用这个） -->
   
  </view>
</template>

<script setup>
// 这里不需要任何import
</script>

<style scoped>
.wrap {
  min-height: 100vh;
  padding: 24rpx;
  box-sizing: border-box;
}
.card {
  background: #2c2c2e;
  border-radius: 16rpx;
  padding: 24rpx;
  margin-bottom: 24rpx;
}
.card-title {
  font-size: 32rpx;
  font-weight: bold;
  color: #fff;
  margin-bottom: 24rpx;
}
.user-header{
  display:flex;
  align-items:center;
  gap:24rpx;
}
.user-info .name{
  font-size:36rpx;
  font-weight:bold;
  color: #fff;
}
.user-info .tip{
  color:#aaa;
  font-size:26rpx;
  margin-top:8rpx;
}
.data-row{
  display:flex;
  justify-content:space-around;
  margin-top:32rpx;
  text-align:center;
}
.data-item .num{
  font-size:36rpx;
  font-weight:bold;
  color:#ffffff;
}
.data-item .label{
  font-size:24rpx;
  color:#aaa;
  margin-top:4rpx;
}
.grid-row{
  display:flex;
  justify-content:space-around;
}
.func-item{
  display:flex;
  flex-direction:column;
  align-items:center;
  gap:12rpx;
  font-size:26rpx;
  color:#fff;
}
.list-item{
  display:flex;
  align-items:center;
  gap:16rpx;
  padding:16rpx 0;
  font-size:30rpx;
  color:#fff;
}

.avatar-img {
  width: 128rpx;
  height: 128rpx;
  border-radius: 50%;
  object-fit: cover;
}
</style>
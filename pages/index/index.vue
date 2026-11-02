<template>
  <view class="page">
    <!-- 顶部 全职/实习/兼职 -->
    <view class="top-tab">
      <view class="tab-item active">日结</view>
     
      <view class="search">
        <text>html5前端...</text>
      </view>
    </view>

    <!-- 分类标签 -->
    <scroll-view scroll-x class="category">
      <view class="cate-item" :class="{active: idx === 0}" v-for="(item,idx) in CategoryTag" :key="idx">{{item.title}}</view>
      <view class="cate-item">+</view>
    </scroll-view>

    <!-- 筛选栏 -->
    <view class="filter-bar">
      <view class="filter-item active">推荐</view>
      <view class="filter-item">附近</view>
      <view class="filter-item">最新</view>
      <view class="filter-right">
        <view class="filter-btn">城市 ▾</view>
        <view class="filter-btn">筛选 ▾</view>
      </view>
    </view>

    <!-- 职位列表 -->
    <scroll-view scroll-y class="list">
      <!-- 卡片1 -->
      <view class="job-card" v-for="(item,idx) in Position" :key="idx">
        <view class="job-title-row">
          <view class="job-name">{{item.title}}</view>
          <view class="job-salary">{{item.Salary}}</view>
        </view>
        <view class="company">{{item.company}} <text class="scale">{{item.scale}}</text></view>
        <view class="bottom-row">
          <view class="recruiter">{{item.HR}}</view>
          <view class="addr">{{item.Place}}</view>
        </view>
      </view>
    </scroll-view>

    <!-- 底部Tabbar -->
 
  </view>
</template>

<script setup>
const CategoryTag=[
	{id:0,title:"综合"},
	{id:1,title:"22"},
]
//工作卡片
const Position=[
	//测试数据
	{id:0,title:"h5前端开发-双休",company:"吧唧哇咔",Salary:"100-130元/天",scale:"未融资 20-99人",HR:"‍李工 · 技术负责人",Place:"广州 番禺区 市桥"},
]
</script>

<style scoped>
.page {
  height: 100vh;
  display: flex;
  flex-direction: column;
  background-color: #1c1c1e;
  color: #fff;
  /* 留出底部tab高度，内容不会被盖住 */
  padding-bottom: 100rpx;
  box-sizing: border-box;
}

/* 顶部全职实习 */
.top-tab {
  display: flex;
  align-items: center;
  padding: 20rpx 30rpx;
  gap: 30rpx;
}
.tab-item {
  font-size: 38rpx;
  color: #aaa;
}
.tab-item.active {
  font-size: 44rpx;
  color: #fff;
  font-weight: bold;
}
.search {
  flex: 1;
  background: #2d2d30;
  border-radius: 99rpx;
  padding: 14rpx 24rpx;
  color: #999;
  font-size:28rpx;
}

/*横向分类标签*/
.category {
  white-space: nowrap;
  padding:0 30rpx;
}
.cate-item {
  display: inline-block;
  font-size:32rpx;
  color:#aaa;
  margin-right:32rpx;
  padding: 8rpx 0;
}
.cate-item.active {
  color:#fff;
  border-bottom:4rpx solid #36c9d0;
}

/*筛选栏*/
.filter-bar {
  display:flex;
  justify-content: space-between;
  padding:20rpx 30rpx;
  align-items:center;
}
.filter-item {
  font-size:30rpx;
  color:#aaa;
  margin-right:30rpx;
}
.filter-item.active {
  color:#fff;
}
.filter-right {
  display:flex;
  gap:20rpx;
}
.filter-btn {
  background:#2d2d30;
  font-size:28rpx;
  padding:10rpx 20rpx;
  border-radius:8rpx;
  color:#ddd;
}

/*职位列表*/
.list {
  flex:1;
  padding:0 30rpx;
}
.job-card {
  background:#2c2c30;
  border-radius:20rpx;
  padding:30rpx;
  margin-bottom:24rpx;
}
.job-title-row {
  display:flex;
  justify-content:space-between;
  margin-bottom:12rpx;
}
.job-name {
  font-size:34rpx;
  font-weight:500;
}
.job-salary {
  color:#4ad1d6;
  font-size:34rpx;
}
.company {
  font-size:28rpx;
  color:#bbbbbb;
  margin-bottom:16rpx;
}
.scale {
  color:#888;
}
.bottom-row {
  display:flex;
  justify-content:space-between;
  font-size:26rpx;
  color:#aaa;
}
</style>
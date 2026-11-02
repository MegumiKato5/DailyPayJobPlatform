<template>
	<view class="tab-bar">
		<view class="tab" @click="onSwitch('index')" :class="{active: current === 'index'}">首页</view>
		<view class="tab" @click="onSwitch('message')" :class="{active: current === 'message'}">消息</view>
		<view class="tab" @click="onSwitch('jobhunting')" :class="{active: current === 'jobhunting'}">我的</view>
	</view>
</template>

<script setup>
const props = defineProps({
	current: {
		type: String,
		default: 'index'
	}
})

const pageMap = {
	index: "/pages/index/index",
	message: "/pages/index/Message",
	jobhunting: "/pages/index/Jobhunting"
}
const onSwitch = (key) => {
	uni.switchTab({
		url: pageMap[key]
	})
}
</script>

<style scoped>
.tab-bar {
	position: fixed;
	bottom: 0;
	left: 0;
	width: 100%;
	height: 100rpx;
	padding-bottom: env(safe-area-inset-bottom);
	background: #2c2c2e;
	display: flex;
	justify-content: space-around;
	align-items: center;
	border-top: 1rpx solid #444;
	z-index: 999;
	box-sizing: border-box;
}
.tab {
	color: #aaa;
	font-size: 28rpx;
}
.tab.active {
	color: #0088cc;
}
</style>
<template>
	<view class="container999">
		<view>在App.vue全局引入common文件夹下的zwyCss.css</view>
		<view>为你想要效果的view添加class  ||  hover-class</view>
		<view class="card">
			<view class="cardItem">
				<view class="tips">波浪背景</view>
				<view>🛒</view>
				<view class="className">zwyWave</view>
			</view>
			<view class="cardItem">
				<view class="tips">流光效果2</view>
				<view class="item1 zwyHeightSec">流光2</view>
				<view class="className">zwyHeightSec</view>
			</view>
			<view class="cardItem">
				<view class="tips">旋转</view>
				<view class="zwyMusic" style="--contentBefore:'♫';--contentAfter:'♩';">
					<view class="bubble zwyRotate" style="animation-duration: 10s;">气泡</view>
				</view>
				<view class="className">zwyRotate zwyMusic</view>
			</view>
			<view class="cardItem">
				<view class="tips">直播头像</view>
				<view class="zwyPortrait" style="--color:#ff0081;">
					<view class="bubble zwyBeat">气泡</view>
				</view>
				<view class="className">zwyPortrait zwyBeat</view>
			</view>
			<view class="cardItem" style="background-color:#4CD964;">
				<view class="tips">直播</view>
				<view style="width: 50rpx;height: 50rpx;display: flex;align-items: center;justify-content: center;">
					<view class="zwyLive" style="--color:white;"></view>
				</view>
				<view class="className">zwyLive</view>
			</view>
			<view class="cardItem">
				<view class="tips">流光效果</view>
				<view class="item1 zwyHeight">流光</view>
				<view class="className">zwyHeight</view>
			</view>
			<view class="cardItem">
				<view class="tips">箭头</view>
				<view class="chevronBox" style="transform: rotate(0deg);">
					<view v-for="(item,index) in 3" :style="{'animation-delay':`${index}s`}" class="zwyChevron" :key="index" ></view>
				</view>
				<view class="className">zwyChevron</view>
			</view>
			<view class="cardItem" style="background-color:#4CD964;">
				<view class="tips">添加黑色波纹</view>
				<!-- color:rgba(0, 0, 0, 0.15); 黑色    color:rgba(255, 255, 255, 0.6); 白色 -->
				<view class="circle zwyHot" style="--color:rgba(0, 0, 0, 0.15);"></view>
				<view class="className">zwyHot</view>
			</view>
			<view class="cardItem" style="background-color:#4CD964;">
				<view class="tips">添加白色波纹</view>
				<view class="circle zwyHot" style="--color:rgba(255, 255, 255, 0.6);"></view>
				<view class="className">zwyHot</view>
			</view>
			<view class="cardItem">
				<view class="tips">缩小点击效果</view>
				<!-- count:Number || infinite -->
				<view class="btn zwyHover1" style="--count:infinite;">按钮</view>
				<view class="className">zwyHover1</view>
			</view>
			<view class="cardItem">
				<view class="tips">摇晃效果</view>
				<!-- transform-origin: top;top:上基准摇晃 bottom:下基准摇晃 -->
				<image class="zwyShake" style="transform-origin: center bottom;width: 40rpx;height: 40rpx;" src="../../static/logo.png"></image>
				<view class="className">zwyShake</view>
			</view>
			<view class="cardItem">
				<view class="tips">气泡点击效果</view>
				<!-- count:Number || infinite; -->
				<view class="btn zwyHover2" style="--color:#ff0081;--count:infinite;">按钮</view>
				<view class="className">zwyHover2</view>
			</view>
			<view class="cardItem">
				<view class="tips">抖动点击效果</view>
				<!-- count:Number || infinite; -->
				<view class="bubble zwyHover3" style="--count:infinite;">气泡</view>
				<view class="className">zwyHover3</view>
			</view>
			<view class="cardItem">
				<view class="tips">浮动效果</view>
				<view class="bubble zwyFly">气泡</view>
				<view class="className">zwyFly</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello'
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style>
	.bubble{
		width: 60rpx;
		height: 60rpx;
		border-radius: 50%;
		background-color: #007AFF;
		color: white;
		text-align: center;
		line-height: 60rpx;
	}
	.tips{
		padding-bottom: 10rpx;
	}
	.className{
		padding-top: 10rpx;
	}
	.circle{
		position: relative;
		box-shadow:0px 6rpx 10rpx 0rpx rgba(106, 168, 194, 0.6);
		background:linear-gradient(-39deg, rgba(43, 161, 250, 1), rgba(156, 210, 252, 1));
		border-radius:50%;
		width: 50rpx;
		height: 50rpx;
	}
	.btn{
		padding: 0 20rpx;
		height: 40rpx;
		border-radius: 40rpx;
		color: white;
		background-color: #007AFF;
	}
	.chevronBox{
		width: 80rpx;
		height: 80rpx;
		background-color: #4CD964;
		display: flex;
		align-items: flex-start;
		justify-content: center;
	}
	.item1{
		background-color: #007AFF;
		padding: 0 20rpx;
		border-radius: 10rpx;
		color: white;
	}
	.cardItem{
		width: 50%;
		display: flex;
		padding: 10rpx 0;
		color: black;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}
	.container999 {
	  width: 100vw;
	  font-size: 28rpx;
	  min-height: 100vh;
	  overflow: hidden;
	  color: #6B8082;
	  position: relative;
	  background-color: #f6f6f6;
	}
	.card{
		width: 91%;
		background-color: white;
		position: relative;
		display: flex;
		flex-wrap:wrap;
		margin: auto;
		border-radius: 5px;
	}
</style>

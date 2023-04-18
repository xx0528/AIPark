<template>
	<view class="park">
		<view class="uni-margin-wrap">
			<swiper class="swiper" circular :indicator-dots="swiperOption.indicatorDots" :autoplay="swiperOption.autoplay" :interval="swiperOption.interval"
				:duration="swiperOption.duration">
				<swiper-item>
					<view class="swiper-item uni-bg-red">A</view>
				</swiper-item>
				<swiper-item>
					<view class="swiper-item uni-bg-green">B</view>
				</swiper-item>
				<swiper-item>
					<view class="swiper-item uni-bg-blue">C</view>
				</swiper-item>
			</swiper>
		</view>
	</view>
	
	<view>
		<uni-grid :column="4" border-color="#03a9f4" @change="change">
			<uni-grid-item :index="0">
				<view class="grid-item-box">
					<image class="image" src="/static/c1.png" mode="aspectFill" />
				</view>
			</uni-grid-item>
			<uni-grid-item :index="1">
				<view class="grid-item-box">
					<image class="image" src="/static/c2.png" mode="aspectFill" />
				</view>
			</uni-grid-item>
			<uni-grid-item :index="2">
				<view class="grid-item-box">
					<image class="image" src="/static/c3.png" mode="aspectFill" />
				</view>
			</uni-grid-item>
			<uni-grid-item :index="3">
				<view class="grid-item-box">
					<image class="image" src="/static/c4.png" mode="aspectFill" />
				</view>
			</uni-grid-item>
		</uni-grid>
	</view>
	
</template>

<script setup>
import { reactive } from "vue";
	const swiperOption = reactive({
		indicatorDots: false,
		autoplay: true,
		interval: 2000,
		duration: 500
	})
</script>

<style lang="scss">
	.uni-margin-wrap {
		padding: 8px;
		.swiper {
			border-radius: 8px;
			overflow: hidden;
			.swiper-item{
				width: 100%;
				height: 100%;
			}
			.uni-bg-red{
				background: red;
			}
			.uni-bg-green{
				background: green;
			}
			.uni-bg-blue{
				background: blue;
			}
		}
		
	}
	
	.fish-grid{
		margin-top: 12upx;
		.grid-box{
			display: flex;
			width: 100%;
			height: 100%;
			align-items: center;
			justify-content: center;
		}
	}
	.image {
		width: 25px;
		height: 25px;
	}
	.grid-item-box {
			flex: 1;
			// position: relative;
			/* #ifndef APP-NVUE */
			display: flex;
			/* #endif */
			flex-direction: column;
			align-items: center;
			justify-content: center;
			padding: 15px 0;
		}
	
</style>

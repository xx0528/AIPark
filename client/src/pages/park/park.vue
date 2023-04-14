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
	
</template>

<script>
import { reactive } from "vue"
	
const swiperOption = reactive({
	indicatorDots: false, 
	autoplay: true,
	interval: 2000,
	duration: 500
})
</script>

<style>
	.uni-margin-wrap{
		padding: 8upx;
		.swiper{
			border-radius: 8upx;
			overflow: hidden;
			.swiper-item{
				width: 100%;
				height: 100%;
			}
			.uni-bg-red {
				background: red;
			}
			.uni-bg-green {
				background: green;
			}
			.uni-bg-yellow{
				background: yellow;
			}
		}
		
	}
	
</style>
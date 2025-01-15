<template>
	<view class="homeLayout">
		<view class="banner">
			<swiper indicator-dots="true" indicator-color="rgba(255,255,255,0.5)"
			indicator-active-color="#fff" autoplay="true" circular="true">
				<swiper-item>
					<image src="/common/images/banner1.jpg" mode="aspectFill"></image>
				</swiper-item>
				<swiper-item>
					<image src="/common/images/banner2.jpg" mode="aspectFill"></image>
				</swiper-item>
				<swiper-item>
					<image src="/common/images/banner3.jpg" mode="aspectFill"></image>
				</swiper-item>
			</swiper>
		</view>
		<view class="notice">
			<view class="left">
				<uni-icons type="sound" size="30" color="#28b389"></uni-icons>
				<text>公告</text>
			</view>
			<view class="center">
				<swiper autoplay="true" circular="true" vertical="true" interval="1500" duration="300" class="center-swipper">
					<swiper-item class="center-swipper-item">
						今日发布：最新版小程序已上线1111111111111
					</swiper-item>
					<swiper-item class="center-swipper-item">
						各位用户如有使用bug 请及时反馈
					</swiper-item>
				</swiper>
		
			</view>
			<view class="right">
				<uni-icons type="checkbox" size="30" color="#28b389"></uni-icons>
			</view>
		</view>
		<view class="select">
			<!-- 标题 -->
			<common-title></common-title>
			<!-- 内容 -->
			<view class="content">
			<scroll-view scroll-x="true" show-scrollbar="true">
				<view class="box" v-for="item in 8 ">
					<image src="/common/images/preview_small.webp" mode="aspectFill"></image>
				</view>
			</scroll-view>
			</view>
		</view>
	</view>
</template>

<script setup>

</script>

<style lang="scss" scoped>
.homeLayout{
	.banner{
		width: 750 rpx;
		padding: 30rpx 0;
		swiper{
			width: 750 rpx;
			height: 340rpx;
			swiper-item{
				padding: 0 30rpx;
				width: 100%;
				height: 100%;
				image{
					width: 100%;
					height: 100%;
					border-radius: 10rpx;
				}
			}
		}
	}
	// 每个部分上下都是相隔30像素
	.notice{
		width: 690rpx;
		height: 80rpx;
		// padding: 30rpx 0;
		background: lightgray;
		margin: 0 auto  ;
		border-radius: 80rpx;
		display: flex;
		line-height: 80rpx;
		.left{
			// margin:  ;
			width: 140rpx;
			display: flex;  //水平居中
			align-items: center; //垂直居中
			justify-content: center;
			text{
				font-weight: bolder;
				color: ghostwhite;
				font-size: 20px;
			}
		}
		.center{
			flex:1;  //左右都加好了 中间加个 flex=1 自动占满
			.center-swipper{
				height: 100%;
				.center-swipper-item{
					height: 100%;
					font-size: 30rpx;
					font-family: "楷体";
					// 超出部分 用... 代替
					overflow: hidden; //超出隐藏
					white-space: nowrap; //不换行
					text-overflow: ellipsis; //省略号
				}
			}
		}
		.right{
			width: 70rpx;
			display: flex;  //水平居中
			align-items: center; //垂直居中
			justify-content: center;
		}
	}
	.select{
		.content{
			
		}
	}
}
</style>

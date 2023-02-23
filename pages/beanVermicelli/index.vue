<template>
	<view class="bean_content">
		<view class="bean_tap">近30天涨了1个新粉丝</view>
		
		<view class="bean_wrap">
			<view class="bean_item">
				<view class="bean_avatar">
					<image src="../../static/images/timg.jpg" mode=""></image>
					<view class="bean_icon">
						<image src="../../static/tabBar/my1.png" mode=""></image>
					</view>
				</view>
				<view class="bean_c_wrap">
					<view class="bean_c_hd">
						<view class="bean_c_name">河马欢乐美食卷</view>
					</view>
					<view class="bean_c_ftr">90后天蝎座男生。重庆工商大学管理系</view>
					<view class="bean_c_ftr">粉丝数 62.8万</view>
				</view>
				<view class="bean_c_button" @click="fansClick">互粉</view>
			</view>
			<view class="bean_item">
				<view class="bean_avatar">
					<image src="../../static/images/timg3.jpg" mode=""></image>
					<view class="bean_icon">
						<image src="../../static/tabBar/my1.png" mode=""></image>
					</view>
				</view>
				<view class="bean_c_wrap">
					<view class="bean_c_hd">
						<view class="bean_c_name">小刚学长</view>
					</view>
					<view class="bean_c_ftr">80后天蝎座男生。重庆工商大学管理系</view>
					<view class="bean_c_ftr">粉丝数 62.8万</view>
				</view>
				<view class="bean_c_button" @click="fansClick">互粉</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
			}
		},
		onLoad() {

		},
		methods: {
			// 互粉
			fansClick(){
				console.log('互粉')
			}

		}
	}
</script>

<style lang="scss" scoped>
	.bean_content{
		.bean_tap{
			width: 100%;
			display: block;
			padding: 30rpx 30rpx;
			box-sizing: border-box;
			font-size: 26rpx;
			color: #a7a7a7;
			font-weight: bold;
		}
		.bean_wrap{
			width: 100%;
			background-color: #ffffff;
			.bean_item{
				width: 100%;
				display: flex;
				align-items: flex-start;
				padding: 30rpx 30rpx;
				box-sizing: border-box;
				.bean_avatar{
					width: 100rpx;
					height: 100rpx;
					position: relative;
					& > image{
						width: 100%;
						height: 100%;
						display: block;
						border-radius: 50%;
					}
					.bean_icon{
						width: 30rpx;
						height: 30rpx;
						border-radius: 50%;
						overflow: hidden;
						border: 4rpx solid #ffffff;
						position: absolute;
						right: 0;
						bottom: 0;
						z-index: 1;
						image{
							width: 100%;
							height: 100%;
							display: block;
						}
					}
				}
				.bean_c_wrap{
					flex: 1;
					padding: 0rpx 20rpx;
					box-sizing: border-box;
					.bean_c_hd{
						width: 100%;
						display: flex;
						align-items: center;
						.bean_c_name{
							font-size: 28rpx;
							color: #333333;
							font-weight: bold;
							margin-right: 10rpx;
						}
					}
					.bean_c_ftr{
						width: 100%;
						font-size: 26rpx;
						color: #a7a7a7;
					}
				}
				.bean_c_button{
					padding: 10rpx 30rpx;
					font-size: 28rpx;
					color: #a7a7a7;
					font-weight: bold;
					border: 1px solid #f2f2f2;
					box-sizing: border-box;
					border-radius: 50rpx;
				}
			}
		}
	}
</style>
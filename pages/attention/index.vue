<template>
	<view class="attention_content">
		<view class="atten_center">
			<view class="atten_c_item">
				<view class="atten_c_avatar">
					<image src="../../static/images/timg.jpg" mode=""></image>
					<view class="atten_c_icon">
						<image src="../../static/tabBar/my1.png" mode=""></image>
					</view>
				</view>
				<view class="atten_c_wrap">
					<view class="atten_c_hd">
						<view class="atten_c_name">小刚学长</view>
						<view class="atten_c_type">微光玩家</view>
					</view>
					<view class="atten_c_ftr">粉丝数 58.1万</view>
				</view>
				<view class="atten_c_button" @click="outAttention">已关注</view>
			</view>
			<view class="atten_c_item">
				<view class="atten_c_avatar">
					<image src="../../static/images/timg.jpg" mode=""></image>
					<view class="atten_c_icon">
						<image src="../../static/tabBar/my1.png" mode=""></image>
					</view>
				</view>
				<view class="atten_c_wrap">
					<view class="atten_c_hd">
						<view class="atten_c_name">河马欢乐美食卷</view>
						<view class="atten_c_type">河马</view>
					</view>
					<view class="atten_c_ftr">粉丝数 62.8万</view>
				</view>
				<view class="atten_c_button" @click="outAttention">已关注</view>
			</view>
			<view class="atten_c_item">
				<view class="atten_c_avatar">
					<image src="../../static/images/timg.jpg" mode=""></image>
					<view class="atten_c_icon">
						<image src="../../static/tabBar/my1.png" mode=""></image>
					</view>
				</view>
				<view class="atten_c_wrap">
					<view class="atten_c_hd">
						<view class="atten_c_name">机智派</view>
						<view class="atten_c_type">机械</view>
					</view>
					<view class="atten_c_ftr">粉丝数 89万</view>
				</view>
				<view class="atten_c_button" @click="outAttention">已关注</view>
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
			// 取消关注
			outAttention(){
				console.log('取消关注')
			}

		}
	}
</script>

<style lang="scss" scoped>
	.attention_content{
		.atten_center{
			width: 100%;
			background-color: #ffffff;
			.atten_c_item{
				width: 100%;
				display: flex;
				align-items: flex-start;
				padding: 30rpx 30rpx;
				box-sizing: border-box;
				.atten_c_avatar{
					width: 100rpx;
					height: 100rpx;
					position: relative;
					& > image{
						width: 100%;
						height: 100%;
						display: block;
						border-radius: 50%;
					}
					.atten_c_icon{
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
				.atten_c_wrap{
					flex: 1;
					padding: 0rpx 20rpx;
					box-sizing: border-box;
					.atten_c_hd{
						width: 100%;
						display: flex;
						align-items: center;
						.atten_c_name{
							font-size: 28rpx;
							color: #333333;
							font-weight: bold;
							margin-right: 10rpx;
						}
						.atten_c_type{
							background-color: rgba(251, 120, 30, .1);
							padding: 0rpx 10rpx;
							box-sizing: border-box;
							border-radius: 50rpx;
							font-size: 22rpx;
							color: #f57766;
						}
					}
					.atten_c_ftr{
						width: 100%;
						font-size: 26rpx;
						color: #a7a7a7;
						margin-top: 20rpx;
					}
				}
				.atten_c_button{
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
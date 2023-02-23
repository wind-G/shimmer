<template>
	<view class="article_list">
		<view class="article_wrap">
			<view class="article_left">
				<view class="article_item">
					<view class="article_photo">
						<image src="../../static/images/timg.jpg" mode="widthFix"></image>
						<text>2次浏览</text>
					</view>
					<view class="article_inner">
						<view class="article_text">走出去玩啊</view>
						<view class="article_ftr">
							<!-- <view class="article_time">6个小时前</view> -->
							<view class="article_f_info">
								<view class="art_f_avatar">
									<image src="../../static/images/timg.jpg" mode=""></image>
								</view>
								<view class="art_f_name">爱百货的小郭</view>
							</view>
							<view class="article_like">
								<image src="../../static/tabBar/my2.png" mode=""></image>
								<!-- <text>1</text> -->
							</view>
						</view>
					</view>
				</view>
			</view>
			<view class="article_right">
				<view class="article_item">
					<view class="article_photo">
						<image src="../../static/images/timg2.jpg" mode="widthFix"></image>
						<text>12次浏览</text>
					</view>
					<view class="article_inner">
						<view class="article_text">走出去玩啊走出去玩啊走出去玩啊走出去玩啊走出去玩啊走出去玩啊走出去玩啊</view>
						<view class="article_ftr">
							<view class="article_time">6个小时前</view>
							<view class="article_like">
								<image src="../../static/tabBar/my1.png" mode=""></image>
								<text>1</text>
							</view>
						</view>
					</view>
				</view>
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

		}
	}
</script>

<style lang="scss" scoped>
	.article_list{
		
		.article_wrap{
			width: 100%;
			display: flex;
			justify-content: space-between;
			padding: 0rpx 30rpx;
			box-sizing: border-box;
			.article_left,
			.article_right{
				width: 48%;
			}
			.article_item{
				width: 100%;
				margin-top: 20rpx;
				.article_photo{
					width: 100%;
					border-radius: 10rpx;
					overflow: hidden;
					position: relative;
					image{
						width: 100%;
						display: block;
					}
					text{
						padding: 3rpx 10rpx;
						border-radius: 5rpx;
						font-size: 20rpx;
						color: #ffffff;
						background-color: rgba(0, 0, 0, .3);
						position: absolute;
						top: 10rpx;
						left: 10rpx;
						z-index: 1;
					}
				}
				.article_inner{
					width: 100%;
					padding: 20rpx 0rpx;
					box-sizing: border-box;
					.article_text{
						width: 100%;
						max-height: 80rpx;
						overflow: hidden;
						font-size: 28rpx;
						color: #333333;
					}
					.article_ftr{
						width: 100%;
						display: flex;
						align-items: center;
						margin-top: 10rpx;
						.article_time{
							flex: 1;
							font-size: 22rpx;
							color: #a7a7a7;
						}
						.article_like{
							padding: 8rpx 10rpx;
							border: 1px solid #a7a7a7;
							border-radius: 50rpx;
							display: flex;
							align-items: center;
							image{
								width: 30rpx;
								height: 30rpx;
							}
							text{
								font-size: 20rpx;
								color: #a7a7a7;
								margin-left: 10rpx;
							}
						}
						.article_f_info{
							flex: 1;
							display: flex;
							align-items: center;
							.art_f_avatar{
								width: 46rpx;
								height: 46rpx;
								border-radius: 50%;
								overflow: hidden;
								margin-right: 10rpx;
								image{
									width: 100%;
									height: 100%;
									display: block;
								}
							}
							.art_f_name{
								font-size: 24rpx;
								color: #a7a7a7;
							}
						}
					}
				}
			}
		}
	}
</style>
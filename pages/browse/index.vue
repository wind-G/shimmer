<template>
	<view class="browse_content">
		<!-- kuai -->
		<view class="bulk100"></view>
		<view class="browse_header">
			<view class="browse_head_title">我浏览的</view>
		</view>
		
		<!-- content -->
		<view class="browse_box">
			<view class="browse_wrap">
				<view class="browse_w_time">2023-02-15</view>
				<view class="browse_w_inner">
					<view class="bro_w_item">
						<view class="bro_w_img">
							<image src="../../static/images/timg.jpg" mode=""></image>
						</view>
						<view class="bro_w_price">￥29.90</view>
					</view>
					<view class="bro_w_item">
						<view class="bro_w_img">
							<image src="../../static/images/timg2.jpg" mode=""></image>
						</view>
						<view class="bro_w_price">￥29.90</view>
					</view>
					<view class="bro_w_item">
						<view class="bro_w_img">
							<image src="../../static/images/timg3.jpg" mode=""></image>
						</view>
						<view class="bro_w_price">￥29.90</view>
					</view>
					<view class="bro_w_item">
						<view class="bro_w_img">
							<image src="../../static/images/banner1.jpg" mode=""></image>
						</view>
						<view class="bro_w_price">￥29.90</view>
					</view>
					<view class="bro_w_item">
						<view class="bro_w_img">
							<image src="../../static/images/list1.jpg" mode=""></image>
						</view>
						<view class="bro_w_price">￥29.90</view>
					</view>
				</view>
			</view>
			<view class="browse_wrap">
				<view class="browse_w_time">2023-02-11</view>
				<view class="browse_w_inner">
					<view class="bro_w_item">
						<view class="bro_w_img">
							<image src="../../static/images/timg.jpg" mode=""></image>
						</view>
						<view class="bro_w_price">￥29.90</view>
					</view>
					<view class="bro_w_item">
						<view class="bro_w_img">
							<image src="../../static/images/timg2.jpg" mode=""></image>
						</view>
						<view class="bro_w_price">￥29.90</view>
					</view>
					<view class="bro_w_item">
						<view class="bro_w_img">
							<image src="../../static/images/timg3.jpg" mode=""></image>
						</view>
						<view class="bro_w_price">￥29.90</view>
					</view>
					<view class="bro_w_item">
						<view class="bro_w_img">
							<image src="../../static/images/banner1.jpg" mode=""></image>
						</view>
						<view class="bro_w_price">￥29.90</view>
					</view>
					<view class="bro_w_item">
						<view class="bro_w_img">
							<image src="../../static/images/list1.jpg" mode=""></image>
						</view>
						<view class="bro_w_price">￥29.90</view>
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
	.browse_content{
		.browse_header{
			width: 100%;
			display: flex;
			align-items: center;
			background-color: #ffffff;
			padding: 30rpx 30rpx;
			box-sizing: border-box;
			position: fixed;
			top: 0;
			left: 0;
			right: 0;
			z-index: 11;
			.browse_head_title{
				font-size: 30rpx;
				color: #333333;
				font-weight: bold;
			}
		}
		.browse_box{
			width: 100%;
			display: block;
			padding: 10rpx 30rpx;
			box-sizing: border-box;
			.browse_wrap{
				.browse_w_time{
					width: 100%;
					display: block;
					font-size: 24rpx;
					color: #a7a7a7;
					padding: 10rpx 5rpx;
					box-sizing: border-box;
				}
				.browse_w_inner{
					width: 100%;
					display: flex;
					flex-wrap: wrap;
					justify-content: flex-start;
					.bro_w_item{
						width: 32%;
						background-color: #ffffff;
						border-radius: 10rpx;
						overflow: hidden;
						margin: 5rpx;
						.bro_w_img{
							width: 100%;
							height: 200rpx;
							display: block;
							image{
								width: 100%;
								height: 100%;
								display: block;
							}
						}
						.bro_w_price{
							width: 100%;
							display: block;
							padding: 15rpx 15rpx;
							box-sizing: border-box;
							font-size: 26rpx;
							color: #ff2525;
							font-weight: bold;
						}
					}
				}
			}
		}
	}
</style>
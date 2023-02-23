<template>
	<view class="meet_content">
		<!-- head -->
		<view class="meet_header">
			<view class="meet_title">消息</view>
			<view class="clear_data" @click="clearClick">
				<image src="../../../static/icon/fanxing.png" mode=""></image>
				清除未读
			</view>
		</view>
		
		<!-- content -->
		<view class="meet_box marginTop">
			<view class="meet_cont_item" @click="chichatClick">
				<view class="meet_c_avatar">
					<image src="../../../static/images/timg2.jpg" mode=""></image>
					<text></text>
				</view>
				<view class="meet_c_wrap">
					<view class="meet_c_name">米西米西</view>
					<view class="meet_c_text">哈哈哈哈喽~</view>
					<view class="meet_c_time">2022-02-08</view>
				</view>
				<view class="meet_c_photo">
					<image src="../../../static/images/timg2.jpg" mode=""></image>
				</view>
			</view>
			<view class="meet_cont_item">
				<view class="meet_c_avatar">
					<image src="../../../static/images/timg.jpg" mode=""></image>
				</view>
				<view class="meet_c_wrap">
					<view class="meet_c_name">梅川酷子</view>
					<view class="meet_c_text">爱搭搭~</view>
					<view class="meet_c_time">2022-02-08</view>
				</view>
				<view class="meet_c_photo">
					<image src="../../../static/images/timg.jpg" mode=""></image>
				</view>
			</view>
			<view class="meet_cont_item">
				<view class="meet_c_avatar">
					<image src="../../../static/images/list1.jpg" mode=""></image>
				</view>
				<view class="meet_c_wrap">
					<view class="meet_c_name">库罗蒂雅</view>
					<view class="meet_c_text">艾弗森法务</view>
					<view class="meet_c_time">2022-02-08</view>
				</view>
				<view class="meet_c_photo">
					<image src="../../../static/images/list1.jpg" mode=""></image>
				</view>
			</view>
			<view class="meet_cont_item">
				<view class="meet_c_avatar">
					<image src="../../../static/images/timg2.jpg" mode=""></image>
				</view>
				<view class="meet_c_wrap">
					<view class="meet_c_name">米西米西</view>
					<view class="meet_c_text">哈哈哈哈喽~</view>
					<view class="meet_c_time">2022-02-08</view>
				</view>
				<view class="meet_c_photo">
					<image src="../../../static/images/timg2.jpg" mode=""></image>
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
			// 清除未读
			clearClick(){
				console.log('正在处理')
			},
			// 消息点击
			chichatClick(){
				uni.navigateTo({
					url:'/pages/chitchat/index'
				})
			}

		}
	}
</script>

<style lang="scss" scoped>
	.meet_content{
		width: 100%;
		display: block;
		.meet_header{
			width: 100%;
			display: flex;
			align-items: center;
			background-color: #ffffff;
			padding: 30rpx 30rpx;
			box-sizing: border-box;
			.meet_title{
				font-size: 40rpx;
				color: #333333;
				font-weight: bold;
				margin-right: 30rpx;
			}
			.clear_data{
				padding: 3rpx 15rpx;
				box-sizing: border-box;
				background-color: #f2f2f2;
				border-radius: 50rpx;
				display: flex;
				align-items: center;
				font-size: 24rpx;
				color: #a7a7a7;
				image{
					width: 40rpx;
					height: 40rpx;
					display: inline-block;
				}
			}
		}
		.meet_box{
			width: 100%;
			display: block;
			background-color: #ffffff;
			.meet_cont_item{
				width: 100%;
				display: flex;
				padding: 30rpx 30rpx;
				box-sizing: border-box;
				.meet_c_avatar{
					width: 100rpx;
					height: 100rpx;
					position: relative;
					image{
						width: 100%;
						height: 100%;
						display: block;
						border-radius: 50%;
					}
					text{
						width: 20rpx;
						height: 20rpx;
						border: 5rpx solid #ffffff;
						display: block;
						background-color: #ff2525;
						border-radius: 50%;
						position: absolute;
						top: 0;
						right: 0;
						z-index: 1;
					}
				}
				.meet_c_wrap{
					flex: 1;
					padding: 0rpx 30rpx;
					box-sizing: border-box;
					.meet_c_name{
						width: 100%;
						font-size: 36rpx;
						color: #515151;
						font-weight: bold;
					}
					.meet_c_text{
						width: 100%;
						display: block;
						font-size: 32rpx;
						color: #a7a7a7;
					}
					.meet_c_time{
						width: 100%;
						display: block;
						font-size: 20rpx;
						color: #a7a7a7;
					}
				}
				.meet_c_photo{
					width: 150rpx;
					height: 150rpx;
					border-radius: 10rpx;
					overflow: hidden;
					image{
						width: 100%;
						height: 100%;
						display: block;
					}
				}
			}
		}
	}
</style>
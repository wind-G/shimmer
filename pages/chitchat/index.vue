<template>
	<view class="chichat_content">
		<!-- kuai -->
		<view class="bulk"></view>
		<view class="bulk"></view>
		<!-- head -->
		<view class="chat_header">
			<view class="chat_head_info">
				<view class="chat_head_avatar">
					<image src="../../static/images/timg.jpg" mode=""></image>
				</view>
				<view class="chat_head_cen">
					<view class="chat_head_name">米西米西</view>
					<view class="chat_head_vip">会员名：l****8</view>
				</view>
			</view>
			
			<view class="chat_commodity">
				<view class="chat_com_photo">
					<image src="../../static/images/timg.jpg" mode=""></image>
				</view>
				<view class="chat_com_wrap">
					<view class="chat_com_inner">
						<view class="chat_com_price">￥5.21</view>
						<view class="chat_com_area">运送方式</view>
						<view class="chat_com_text">交易前聊一聊</view>
					</view>
					<view class="chat_com_but" @click="purchaseClick">立即购买</view>
				</view>
			</view>
		</view>
		
		<!-- content -->
		<view class="chat_contain">
			<view class="chat_cont_time">13:12</view>
			<view class="chat_cont_one">
				<view class="chat_cont_avatar">
					<image src="../../static/images/timg.jpg" mode=""></image>
				</view>
				<view class="chat_cont_wrap">
					<!-- 文字 -->
					<view class="chat_cont_word">今日感受夏天温柔的风，我记得我吹过，保持愉悦健康的生活姿态，努力迎接每一天带来的惊喜，加油</view>
					<!-- 图片 -->
					<!-- <view class="chat_cont_photo">
						<image src="../../static/images/timg.jpg" mode="widthFix"></image>
					</view> -->
				</view>
			</view>
			<view class="chat_cont_two">
				<view class="chat_cont_wrap">
					<!-- 文字 -->
					<!-- <view class="chat_cont_word">今日感受夏天温柔的风，我记得我吹过，保持愉悦健康的生活姿态，努力迎接每一天带来的惊喜，加油</view> -->
					<!-- 图片 -->
					<view class="chat_cont_photo">
						<image src="../../static/images/timg.jpg" mode="widthFix"></image>
					</view>
				</view>
				<view class="chat_cont_avatar">
					<image src="../../static/images/timg.jpg" mode=""></image>
				</view>
			</view>
		</view>
		
		<!-- 对话框 -->
		<view class="chat_dialog">
			<view class="chat_dialog_input">
				<input type="text" placeholder="想跟他说什么...">
			</view>
			<view class="chat_dialog_right">
				<view class="chat_dia_item">
					<image src="../../static/tabBar/personal2.png" mode=""></image>
				</view>
				<view class="chat_dia_item">
					<image src="../../static/icon/add.png" mode=""></image>
				</view>
			</view>
		</view>
		
		<!-- kuai -->
		<view class="bulk"></view>
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
			// 购买微光
			purchaseClick(){
				uni.navigateTo({
					url: '/pages/purchase/index'
				})
			}
		}
	}
</script>

<style lang="scss" scoped>
	.chichat_content{
		width: 100%;
		display: block;
		.chat_header{
			width: 100%;
			background-color: #f2f2f2;
			position: fixed;
			top: 0;
			left: 0;
			right: 0;
			z-index: 11;
			border-bottom: 1px solid #e7e7e7;
		}
		.chat_head_info{
			width: 100%;
			display: flex;
			align-items: center;
			padding: 30rpx 30rpx;
			box-sizing: border-box;
			.chat_head_avatar{
				width: 80rpx;
				height: 80rpx;
				border-radius: 50%;
				overflow: hidden;
				margin-right: 15rpx;
				image{
					width: 100%;
					height: 100%;
					display: block;
				}
			}
			.chat_head_cen{
				flex: 1;
				.chat_head_name{
					width: 100%;
					font-size: 40rpx;
					color: #333333;
					font-weight: bold;
				}
				.chat_head_vip{
					width: 100%;
					display: block;
					font-size: 20rpx;
					color: #a7a7a7;
				}
			}
		}
		.chat_commodity{
			width: 100%;
			display: flex;
			padding: 0rpx 30rpx 30rpx;
			box-sizing: border-box;
			.chat_com_photo{
				width: 120rpx;
				height: 120rpx;
				border-radius: 10rpx;
				overflow: hidden;
				image{
					width: 100%;
					height: 100%;
					display: block;
				}
			}
			.chat_com_wrap{
				flex: 1;
				display: flex;
				align-items: flex-end;
				padding-left: 20rpx;
				box-sizing: border-box;
				.chat_com_inner{
					flex: 1;
					.chat_com_price{
						width: 100%;
						font-size: 28rpx;
						color: #ff2525;
						font-weight: bold;
					}
					.chat_com_area,
					.chat_com_text{
						width: 100%;
						display: block;
						font-size: 20rpx;
						color: #a7a7a7;
					}
				}
				.chat_com_but{
					width: 210rpx;
					height: 70rpx;
					line-height: 70rpx;
					text-align: center;
					background-color: #ff2525;
					font-size: 28rpx;
					font-weight: bold;
					color: #ffffff;
					border-radius: 50rpx;
					box-shadow: 0rpx 5rpx 15rpx #a7a7a7;
				}
			}
		}
		.chat_contain{
			width: 100%;
			// max-height: 60%;
			// background-color: #FCCA00;
			display: block;
			padding: 30rpx 30rpx;
			box-sizing: border-box;
			.chat_cont_time{
				width: 100%;
				text-align: center;
				font-size: 24rpx;
				color: #a7a7a7;
				padding: 30rpx 30rpx;
				box-sizing: border-box;
			}
			.chat_cont_one,
			.chat_cont_two{
				width: 100%;
				display: flex;
				padding: 20rpx 0rpx;
				box-sizing: border-box;
			}
			.chat_cont_avatar{
				width: 70rpx;
				height: 70rpx;
				border-radius: 50%;
				overflow: hidden;
				image{
					width: 100%;
					height: 100%;
					display: block;
				}
			}
			.chat_cont_wrap{
				flex: 1;
				display: flex;
				.chat_cont_word{
					border-radius: 10rpx;
					padding: 5rpx 20rpx;
					box-sizing: border-box;
					font-size: 24rpx;
					color: #333333;
				}
				.chat_cont_photo{
					max-width: 200rpx;
					max-height: 200rpx;
					display: flex;
					border-radius: 10rpx;
					overflow: hidden;
					image{
						max-width: 100%;
						max-height: 100%;
						display: block;
					}
				}
			}
			
			
			
			.chat_cont_one{
				.chat_cont_avatar{
					margin-right: 20rpx;
				}
				.chat_cont_wrap{
					justify-content:flex-start;
					padding-right: 80rpx;
					.chat_cont_word{
						background-color: #ffffff;
					}
				}
			}
			.chat_cont_two{
				.chat_cont_avatar{
					margin-left: 20rpx;
				}
				.chat_cont_wrap{
					justify-content:flex-end;
					padding-left: 80rpx;
					.chat_cont_word{
						background-color: #FCCA00;
					}
				}
			}
		}
		.chat_dialog{
			width: 100%;
			display: flex;
			align-items: center;
			padding: 30rpx 30rpx;
			box-sizing: border-box;
			background-color: #f2f2f2;
			position: fixed;
			left: 0;
			right: 0;
			bottom: 0;
			z-index: 11;
			.chat_dialog_input{
				flex: 1;
				height: 70rpx;
				background-color: #ffffff;
				border-radius: 50rpx;
				input{
					width: 100%;
					height: 100%;
					display: block;
					border: 0;
					outline: none;
					padding: 0rpx 30rpx;
					box-sizing: border-box;
					font-size: 26rpx;
					color: #333333;
				}
			}
			.chat_dialog_right{
				display: flex;
				align-items: center;
				.chat_dia_item{
					width: 50rpx;
					height: 50rpx;
					margin-left: 30rpx;
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
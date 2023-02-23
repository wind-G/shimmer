<template>
	<view class="play_content">
		<!-- head -->
		<view class="play_header">
			<view class="play_avatar">
				<image src="@/static/images/timg3.jpg" mode=""></image>
			</view>
			<view class="play_name">仙乐的钰</view>
			<view class="pro_info_button">
				<text>+&nbsp;关注</text>
			</view>
		</view>
		
		<!-- 内容 -->
		<view class="play_inner">
			<view class="play_banner">
				<swiper class="swiper" circular :indicator-dots="indicatorDots" :autoplay="autoplay" :interval="interval" :duration="duration">
					<swiper-item>
						<view class="play_ba_item">
							<image src="../../static/images/timg.jpg" mode="widthFix"></image>
						</view>
					</swiper-item>
					<swiper-item>
						<view class="play_ba_item">
							<image src="../../static/images/list1.jpg" mode="widthFix"></image>
						</view>
					</swiper-item>
					<swiper-item>
						<view class="play_ba_item">
							<image src="../../static/images/timg2.jpg" mode="widthFix"></image>
						</view>
					</swiper-item>
				</swiper>
			</view>
			<view class="play_tell">
				运动项目瑜伽运动普拉提
				<br/>
				分运动时长60分钟
				<br/>
				9今日感受夏天温柔的风，我记得我吹过，保持愉悦健康的生活姿态，努力迎接每一天带来的惊喜，加油!
			</view>
			<view class="play_time">10-22</view>
		</view>
		
		<!-- 评论 -->
		<view class="play_comment marginTop">
			<view class="p_com_title">全部评论·535</view>
			<view class="p_com_wrap">
				<view class="p_com_item marginTop">
					<view class="p_com_avatar">
						<image src="../../static/images/timg.jpg" mode=""></image>
					</view>
					<view class="com_it_inner com_it_line">
						<view class="com_it_info">
							<view class="com_it_cont">
								<view class="com_in_hd">
									<view class="msg_in_name">南京伊人</view>
									<view class="msg_in_time">·1小时前</view>
									<view class="msg_in_area">南京</view>
								</view>
								<view class="msg_in_text">我喜欢你你喜欢我吗？</view>
							</view>
							<view class="msg_inter_state">
								<image class="msg_inter_btn" src="../../static/tabBar/my2.png" mode=""></image>
								34
							</view>
						</view>
						<view class="com_it_wrap">
							<view class="com_it_item marginTop">
								<view class="com_i_avatar">
									<image src="../../static/images/timg.jpg" mode=""></image>
								</view>
								<view class="com_it_inner">
									<view class="com_it_info">
										<view class="com_it_cont">
											<view class="com_in_hd">
												<view class="msg_in_name">花开四季</view>
												<view class="msg_in_time">·1小时前</view>
												<view class="msg_in_area">天津</view>
											</view>
											<view class="msg_in_text">
												回复了<text>南京伊人</text>:
												我喜欢你
											</view>
										</view>
										<view class="msg_inter_state">
											<image class="msg_inter_btn" src="../../static/tabBar/my2.png" mode=""></image>
											2
										</view>
									</view>
								</view>
							</view>
							<view class="com_it_item marginTop">
								<view class="com_i_avatar">
									<image src="../../static/images/timg.jpg" mode=""></image>
								</view>
								<view class="com_it_inner">
									<view class="com_it_info">
										<view class="com_it_cont">
											<view class="com_in_hd">
												<view class="msg_in_name">南方花园</view>
												<view class="msg_in_time">·20分钟前</view>
												<view class="msg_in_area">北京</view>
											</view>
											<view class="msg_in_text">
												回复了<text>南京伊人</text>:
												我也喜欢，爱你哟
											</view>
										</view>
										<view class="msg_inter_state">
											<image class="msg_inter_btn" src="../../static/tabBar/my2.png" mode=""></image>
											2
										</view>
									</view>
								</view>
							</view>
							<view class="com_it_item marginTop">
								<view class="com_i_avatar">
									<image src="../../static/images/timg.jpg" mode=""></image>
								</view>
								<view class="com_it_inner">
									<view class="com_it_info">
										<view class="com_it_cont">
											<view class="com_in_hd">
												<view class="msg_in_name">南京伊人</view>
												<view class="msg_in_time">·10分钟前</view>
												<view class="msg_in_area">南京</view>
											</view>
											<view class="msg_in_text">
												回复了<text>南方花园</text>:
												我也喜欢你
											</view>
										</view>
										<view class="msg_inter_state">
											<image class="msg_inter_btn" src="../../static/tabBar/my2.png" mode=""></image>
											2
										</view>
									</view>
								</view>
							</view>
							
							<view class="com_it_lock marginTop">查看33条回复</view>
						</view>
					</view>
				</view>
			
				<view class="msg_inter_all marginTop">
					查看更多评论&nbsp;&RightAngleBracket;
				</view>
			</view>
			<!-- 对话框 -->
			<view class="play_dialog" :style="{position: dialogState}">
				<view class="p_dialog_input">
					<input type="text" placeholder="喜欢就说两句">
				</view>
				<view class="p_dialog_right">
					<view class="p_dia_item">
						<image src="../../static/tabBar/personal2.png" mode=""></image>
						<text>344</text>
					</view>
					<view class="p_dia_item">
						<image src="../../static/tabBar/meet2.png" mode=""></image>
						<text>344</text>
					</view>
					<view class="p_dia_item">
						<image src="../../static/tabBar/my2.png" mode=""></image>
						<text>344</text>
					</view>
				</view>
			</view>
		</view>
		
		<!-- kuai -->
		<!-- <view class="bulk"></view> -->
	</view>
</template>

<script>
	export default {
		data() {
			return {
				indicatorDots: true,
				autoplay: true,
				interval: 2000,
				duration: 1000,
				dialogState: 'fixed', // 对话框状态
			}
		},
		onLoad() {
		},
		onPageScroll(e) {
			// 元素距离屏幕的高度
			let that = this;
			uni.getSystemInfo({
				success: resu => {
					// resu 可以获取当前屏幕的高度
					const query = uni.createSelectorQuery();
					query.select('.p_com_wrap').boundingClientRect();
					query.exec(res => {
						// console.log(res[0].height)
						let top = (res[0].top + res[0].height) - resu.windowHeight;
						console.log(res[0].height)
						if(top <= 10){
							this.dialogState = 'relative'
						}else{
							this.dialogState = 'fixed'
						}
					})
				}
			})
		},
		methods: {
			// 元素距离屏幕的高度
			dialogHight(){
			}
		}
	}
</script>

<style lang="scss" scoped>
	.play_content{
		width: 100%;
		display: block;
		.play_header{
			width: 100%;
			display: flex;
			align-items: center;
			background-color: #ffffff;
			padding: 30rpx 30rpx;
			box-sizing: border-box;
			.play_avatar{
				width: 60rpx;
				height: 60rpx;
				display: inline-block;
				border-radius: 50%;
				overflow: hidden;
				margin-right: 10rpx;
				image{
					width: 100%;
					height: 100%;
					display: block;
				}
			}
			.play_name{
				flex: 1;
				font-size: 30rpx;
				color: #333333;
				font-weight: bold;
			}
			// 关注
			.pro_info_button{
				padding: 10rpx 20rpx;
				box-sizing: border-box;
				background-color: #f2f2f2;
				border-radius: 50rpx;
				font-size: 26rpx;
				color: #333333;
				font-weight: bold;
			}
		}
		// 内容
		.play_inner{
			width: 100%;
			display: block;
			background-color: #ffffff;
			.play_banner{
				width: 100%;
				display: block;
				.swiper{
					width: 100%;
					height: 800rpx;
					overflow: hidden;
					.play_ba_item{
						width: 100%;
						height: 100%;
						display: flex;
						align-items: center;
						justify-content: center;
						image{
							width: 100%;
							max-width: 100%;
							max-height: 100%;
							display: block;
						}
					}
				}
			}
			.play_tell{
				width: 100%;
				padding: 30rpx 30rpx;
				box-sizing: border-box;
				display: block;
			}
			.play_time{
				width: 100%;
				padding: 0rpx 30rpx 30rpx;
				box-sizing: border-box;
				font-size: 20rpx;
				color: #a7a7a7;
			}
		}
		
		// 评论
		.play_comment{
			width: 100%;
			display: block;
			background-color: #ffffff;
			.p_com_title{
				font-size: 30rpx;
				color: #333333;
				font-weight: bold;
				padding: 30rpx 30rpx;
				box-sizing: border-box;
			}
			.p_com_wrap{
				width: 100%;
				padding: 30rpx 30rpx;
				box-sizing: border-box;
				display: block;
				.p_com_item{
					width: 100%;
					display: flex;
					.p_com_avatar{
						width: 60rpx;
						height: 60rpx;
					}
					.com_i_avatar{
						width: 46rpx;
						height: 46rpx;
					}
					.p_com_avatar,
					.com_i_avatar{
						border-radius: 50%;
						overflow: hidden;
						margin-right: 10rpx;
						image{
							width: 100%;
							height: 100%;
							display: block;
						}
					}
					.com_it_line{
						border-bottom: 1px solid #f2f2f2;
						padding-bottom: 20rpx;
						box-sizing: border-box;
					}
					.com_it_inner{
						flex: 1;
						.com_it_info{
							width: 100%;
							display: flex;
							align-items: center;
							.com_it_cont{
								flex: 1;
								.com_in_hd{
									width: 100%;
									display: flex;
									align-items: center;
									.msg_in_name{
										font-size: 28rpx;
										color: #666666;
										font-weight: bold;
									}
									.msg_in_time{
										font-size: 20rpx;
										color: #a7a7a7;
									}
									.msg_in_area{
										background-color: #f2f2f2;
										font-size: 20rpx;
										color: #a7a7a7;
										border-radius: 3rpx;
										padding: 0rpx 10rpx;
										box-sizing: border-box;
										margin-left: 10rpx;
									}
								}
								.msg_in_text{
									width: 100%;
									display: block;
									font-size: 26rpx;
									color: #333333;
									margin-top: 10rpx;
									text{
										color: #a7a7a7;
										font-weight: bold;
									}
								}
							}
							.msg_inter_state{
								text-align: center;
								font-size: 20rpx;
								color: #a7a7a7;
								.msg_inter_btn{
									width: 40rpx;
									height: 40rpx;
									display: block;
									margin-bottom: 5rpx;
								}
							}
						}
						// 
						.com_it_wrap{
							width: 100%;
							display: block;
							.com_it_item{
								width: 100%;
								display: flex;
							}
							.com_it_lock{
								width: 100%;
								display: block;
								font-size: 28rpx;
								color: #1296db;
								font-weight: bold;
								padding: 0rpx 56rpx;
								box-sizing: border-box;
							}
						}
					}
				}
				.msg_inter_all{
					width: 100%;
					text-align: center;
					font-size: 28rpx;
					color: #a7a7a7;
					font-weight: bold;
				}
			}
			// 对话框
			.play_dialog{
				width: 100%;
				padding: 30rpx 30rpx;
				display: flex;
				align-items: center;
				background-color: #ffffff;
				box-sizing: border-box;
				left: 0;
				right: 0;
				bottom: 0;
				z-index: 11;
				.p_dialog_input{
					flex: 1;
					height: 70rpx;
					background-color: #f2f2f2;
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
				.p_dialog_right{
					display: flex;
					align-items: center;
					.p_dia_item{
						font-size: 20rpx;
						color: #a7a7a7;
						text-align: center;
						margin-left: 40rpx;
						image{
							width: 46rpx;
							height: 46rpx;
							display: block;
							margin: auto;
						}
						text{
							margin-top: 5rpx;
						}
					}
				}
			}
		}
		
	}
</style>
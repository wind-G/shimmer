<template>
	<view class="personal_content">
		<view class="personal_info" @click="homePageClick">
			<view class="per_info_avatar">
				<image src="../../../static/images/timg.jpg" mode=""></image>
			</view>
			<view class="per_info_wrap">
				<view class="per_info_name">昵称未设置</view>
				<view class="per_info_vip">
					会员名：t***9
				</view>
			</view>
		</view>
		<view class="personal_type">
			<view class="per_type_item" @click="collectClick">
				<text>0</text>
				收藏
			</view>
			<view class="per_type_item" @click="browseClick">
				<text>24</text>
				历史浏览
			</view>
			<view class="per_type_item" @click="attentionClick">
				<text>0</text>
				关注
			</view>
			<view class="per_type_item" @click="beanClick">
				<text>0</text>
				粉丝
			</view>
			<view class="per_type_item" @click="articleClick">
				<text>0</text>
				帖子
			</view>
		</view>
		
		<view class="personal_tran marginTop">
			<view class="per_tran_title">我的交易</view>
			<view class="per_tran_wrap marginTop">
				<view class="per_tran_item">
					<view class="per_tran_img">
						<image src="../../../static/images/hyq.png" mode=""></image>
					</view>
					<view class="per_tran_title">我发布的 0</view>
				</view>
				<view class="per_tran_item">
					<view class="per_tran_img">
						<image src="../../../static/images/jkzx.png" mode=""></image>
					</view>
					<view class="per_tran_title">我卖出的 0</view>
				</view>
				<view class="per_tran_item">
					<view class="per_tran_img">
						<image src="../../../static/images/tupian.png" mode=""></image>
					</view>
					<view class="per_tran_title">我买到的 0</view>
				</view>
				<view class="per_tran_item">
					<view class="per_tran_img">
						<image src="../../../static/images/work1.png" mode=""></image>
					</view>
					<view class="per_tran_title">我抢购的 0</view>
				</view>
			</view>
		</view>
		
		<view class="personal_equity">
			<view class="per_tran_title">互动权益</view>
			<view class="per_equity_wrap">
				<view class="per_equity_item">
					<view class="per_equity_img">
						<image src="../../../static/images/icon-cjwt.png" mode=""></image>
					</view>
					<view class="per_equity_title">问题投诉</view>
				</view>
				<view class="per_equity_item">
					<view class="per_equity_img">
						<image src="../../../static/images/icon-fxyl.png" mode=""></image>
					</view>
					<view class="per_equity_title">推荐分享</view>
				</view>
				<view class="per_equity_item">
					<view class="per_equity_img">
						<image src="../../../static/images/icon-jkda.png" mode=""></image>
					</view>
					<view class="per_equity_title">实名认证</view>
				</view>
				<view class="per_equity_item">
					<view class="per_equity_img">
						<image src="../../../static/images/icon-kefu.png" mode=""></image>
					</view>
					<view class="per_equity_title">客服服务</view>
				</view>
				<view class="per_equity_item">
					<view class="per_equity_img">
						<image src="../../../static/images/icon-shdz.png" mode=""></image>
					</view>
					<view class="per_equity_title">添加地址</view>
				</view>
				<view class="per_equity_item" @click="settingClick">
					<view class="per_equity_img">
						<image src="../../../static/images/icon-shezhi.png" mode=""></image>
					</view>
					<view class="per_equity_title">设置</view>
				</view>
				<view class="per_equity_item">
					<view class="per_equity_img">
						<image src="../../../static/images/icon-ry6.png" mode=""></image>
					</view>
					<view class="per_equity_title">我的勋章</view>
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
			// 个人主页
			homePageClick(){
				uni.navigateTo({
					url: '/pages/homePage/index'
				})
			},
			// 收藏
			collectClick(){
				uni.navigateTo({
					url: '/pages/collect/index'
				})
			},
			// 历史浏览
			browseClick(){
				uni.navigateTo({
					url: '/pages/browse/index'
				})
			},
			// 我的关注
			attentionClick(){
				uni.navigateTo({
					url: '/pages/attention/index'
				})
			},
			// 我的粉丝
			beanClick(){
				uni.navigateTo({
					url: '/pages/beanVermicelli/index'
				})
			},
			// 我的帖子
			articleClick(){
				uni.navigateTo({
					url: '/pages/article/index'
				})
			},
			// 设置
			settingClick(){
				uni.navigateTo({
					url: '/pages/settingUp/index'
				})
			}
		}
	}
</script>

<style lang="scss" scoped>
	.personal_content{
		width: 100%;
		display: block;
	}
	.personal_info{
		width: 100%;
		display: flex;
		align-items: center;
		background-color: #ffffff;
		padding: 30rpx 30rpx 20rpx;
		box-sizing: border-box;
		.per_info_avatar{
			width: 150rpx;
			height: 150rpx;
			border-radius: 50%;
			overflow: hidden;
			image{
				width: 100%;
				height: 100%;
				display: block;
			}
		}
		.per_info_wrap{
			flex: 1;
			padding-left: 20rpx;
			box-sizing: border-box;
			.per_info_name{
				width: 100%;
				font-size: 38rpx;
				color: #333333;
				font-weight: bold;
			}
			.per_info_vip{
				width: 100%;
				display: block;
				font-size: 24rpx;
				color: #a7a7a7;
			}
		}
	}
	.personal_type{
		width: 100%;
		display: flex;
		align-items: center;
		justify-content: space-between;
		background-color: #ffffff;
		.per_type_item{
			width: 20%;
			padding: 30rpx 15rpx;
			box-sizing: border-box;
			text-align: center;
			font-size: 24rpx;
			color: #333333;
			text{
				width: 100%;
				display: block;
				font-size: 32rpx;
				font-weight: bold;
			}
		}
	}
	.personal_tran{
		width: 100%;
		background-color: #ffffff;
		padding: 30rpx 0rpx;
		box-sizing: border-box;
		.per_tran_wrap{
			width: 100%;
			display: flex;
			justify-content: space-between;
			align-items: center;
			.per_tran_item{
				width: 25%;
				.per_tran_img{
					width: 80rpx;
					height: 80rpx;
					display: block;
					margin: auto;
					image{
						width: 100%;
						height: 100%;
						display: block;
					}
				}
				.per_tran_title{
					width: 100%;
					text-align: center;
					font-size: 24rpx;
					color: #333333;
				}
			}
		}
	}
	.personal_equity{
		width: 100%;
		background-color: #ffffff;
		padding: 30rpx 0rpx;
		box-sizing: border-box;
		.per_equity_wrap{
			width: 100%;
			display: flex;
			flex-wrap: wrap;
			justify-content: flex-start;
			.per_equity_item{
				width: 25%;
				text-align: center;
				padding: 15rpx 0rpx;
				box-sizing: border-box;
				.per_equity_img{
					width: 70rpx;
					height: 70rpx;
					display: block;
					margin: auto;
					image{
						width: 100%;
						height: 100%;
						display: block;
					}
				}
				.per_equity_title{
					width: 100%;
					text-align: center;
					font-size: 24rpx;
					color: #333333;
				}
			}
		}
	}
	.per_tran_title{
		width: 100%;
		padding: 0rpx 30rpx;
		box-sizing: border-box;
		font-size: 30rpx;
		color: #333333;
		font-weight: bold;
	}
</style>
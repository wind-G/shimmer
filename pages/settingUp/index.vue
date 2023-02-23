<template>
	<view class="setting_up">
			<view class="setting_box">
				<view class="setting_wrap">
					<view class="set_wrap_item" @click="infoClick">
						<view class="set_wrap_tit">个人资料设置</view>
						<image src="../../static/icon/jright.png" mode=""></image>
					</view>
					<view class="set_wrap_item" @click="addressClick">
						<view class="set_wrap_tit">地址管理</view>
						<image src="../../static/icon/jright.png" mode=""></image>
					</view>
					<view class="set_wrap_item">
						<view class="set_wrap_tit">账户安全</view>
						<image src="../../static/icon/jright.png" mode=""></image>
					</view>
					<view class="set_wrap_item">
						<view class="set_wrap_tit">黑名单</view>
						<image src="../../static/icon/jright.png" mode=""></image>
					</view>
					<view class="set_wrap_item">
						<view class="set_wrap_tit">我的二维码</view>
						<image src="../../static/icon/jright.png" mode=""></image>
					</view>
					<view class="set_wrap_item">
						<view class="set_wrap_tit">全局自动回复设置</view>
						<image src="../../static/icon/jright.png" mode=""></image>
					</view>
				</view>
				<view class="setting_wrap marginTop">
					<view class="set_wrap_item">
						<view class="set_wrap_tit">关于</view>
						<image src="../../static/icon/jright.png" mode=""></image>
					</view>
					<view class="set_wrap_item">
						<view class="set_wrap_tit">分享</view>
						<image src="../../static/icon/jright.png" mode=""></image>
					</view>
					<view class="set_wrap_item">
						<view class="set_wrap_tit">安全中心</view>
						<image src="../../static/icon/jright.png" mode=""></image>
					</view>
					<view class="set_wrap_item">
						<view class="set_wrap_tit">清除缓存</view>
						<image src="../../static/icon/jright.png" mode=""></image>
					</view>
				</view>
			</view>
			
			<view class="out_login_box">
				<view class="out_login">退出登录</view>
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
			// 个人资料设置
			infoClick(){
				uni.navigateTo({
					url: '/pages/information/index'
				})
			},
			// 地址管理
			addressClick(){
				uni.navigateTo({
					url: '/pages/address/index'
				})
			}

		}
	}
</script>

<style lang="scss" scoped>
	.setting_box{
		width: 100%;
		display: block;
		.setting_wrap{
			width: 100%;
			background-color: #ffffff;
			padding: 0rpx 30rpx;
			box-sizing: border-box;
			.set_wrap_item{
				width: 100%;
				display: flex;
				align-items: center;
				border-bottom: 1px solid #f2f2f2;
				padding: 30rpx 0rpx;
				box-sizing: border-box;
				.set_wrap_tit{
					flex: 1;
					font-size: 28rpx;
					color: #333333;
					font-weight: bold;
				}
				image{
					width: 30rpx;
					height: 30rpx;
					display: block;
				}
			}
		}
	}
	.out_login_box{
		width: 100%;
		display: block;
		padding: 30rpx 30rpx;
		box-sizing: border-box;
		.out_login{ 
			width: 100%;
			height: 80rpx;
			line-height: 80rpx;
			display: block;
			text-align: center;
			background-color: #ff2525;
			border-radius: 50rpx;
			font-size: 32rpx;
			color: #ffffff;
			box-shadow: 0rpx 5rpx 15rpx #a7a7a7;
		}
	}
</style>
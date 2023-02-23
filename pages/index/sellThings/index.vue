<template>
	<view class="sell_content">
		<view class="sell_box">
			<view class="bulk150"></view>
			<view class="sell_item sell_yellow" @click="stockClick">
				<image class="sell_i_img" src="../../../static/images/fenshi.png" mode=""></image>
				<view class="sell_i_cont">
					<view class="sell_i_tit">上架微光</view>
					<view class="sell_i_txt">快速发布宝贝,以微光在黑夜中闪闪发亮</view>
				</view>
				<image class="sell_i_icon" src="../../../static/icon/jright2.png" mode=""></image>
			</view>
			<view class="sell_item sell_bule" @click="lifeClick">
				<image class="sell_i_img" src="../../../static/images/shouchang.png" mode=""></image>
				<view class="sell_i_cont">
					<view class="sell_i_tit">发布星光</view>
					<view class="sell_i_txt">分享我的生活,以星光照耀着他人</view>
				</view>
				<image class="sell_i_icon" src="../../../static/icon/jright2.png" mode=""></image>
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
			// 上架微光
			stockClick(){
				uni.navigateTo({
					url: '/pages/newStock/index'
				})
			},
			// 发布星光
			lifeClick(){
				uni.navigateTo({
					url: '/pages/shareMyLife/index'
				})
			}

		}
	}
</script>

<style lang="scss" scoped>
	.sell_box{
		width: 100%;
		display: flex;
		flex-wrap: wrap;
		flex-direction: column-reverse;
		background-color: #ffffff;
		padding: 30rpx 30rpx;
		box-sizing: border-box;
		position: fixed;
		top: 0;
		left: 0;
		right: 0;
		bottom: 0;
		.sell_yellow{
			background-color: rgba(255, 230, 15, 1);
		}
		.sell_pink{
			background-color: rgba(251, 120, 109, 0.2);
		}
		.sell_bule{
			background-color: rgba(220, 250, 252, 0.5);
		}
		.sell_item{
			width: 100%;
			display: flex;
			align-items: center;
			border-radius: 10rpx;
			margin: 10rpx 0rpx;
			padding: 30rpx 30rpx;
			box-sizing: border-box;
			.sell_i_img{
				width: 100rpx;
				height: 100rpx;
			}
			.sell_i_cont{
				flex: 1;
				padding: 0rpx 30rpx;
				box-sizing: border-box;
				.sell_i_tit{
					width: 100%;
					font-size: 32rpx;
					color: #333333;
					font-weight: bold;
				}
				.sell_i_txt{
					width: 100%;
					font-size: 24rpx;
					color: #a7a7a7;
				}
			}
			.sell_i_icon{
				width: 40rpx;
				height: 40rpx;
			}
		}
	}
</style>
<template>
	<view class="search_cephalic">
		<view class="search_header">
			<view class="sea_hd_wrap">
				<view class="sea_hd_return">
					<image src="../../static/icon/jleft.png" mode=""></image>
				</view>
				<view class="sea_hd_center">
					<image class="sea_hd_icon" src="../../static/icon/icon-fangdajing.png" mode=""></image>
					<input type="text" placeholder="搜索宝贝/帖子/用户">
				</view>
				<view class="sea_hd_button">搜索</view>
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
	.search_cephalic{
		
		.search_header{
			width: 100%;
			display: block;
			padding: 0rpx 30rpx;
			box-sizing: border-box;
			.sea_hd_wrap{
				width: 100%;
				display: flex;
				align-items: center;
				.sea_hd_return{
					width: 46rpx;
					height: 46rpx;
					margin-right: 10rpx;
					image{
						width: 100%;
						height: 100%;
						display: block;
					}
				}
				.sea_hd_center{
					flex: 1;
					height: 64rpx;
					line-height: 64rpx;
					border: 6rpx solid #FCCA00;
					border-radius: 50rpx;
					position: relative;
					.sea_hd_icon{
						width: 36rpx;
						height: 36rpx;
						display: block;
						position: absolute;
						top: 0;
						left: 20rpx;
						bottom: 0;
						margin: auto;
					}
					input{
						width: 100%;
						height: 100%;
						display: block;
						border: 0;
						outline: none;
						padding-left: 80rpx;
						padding-right: 30rpx;
						box-sizing: border-box;
						font-size: 26rpx;
						color: #333333;
					}
				}
				.sea_hd_button{
					font-size: 32rpx;
					color: #333333;
					font-weight: bold;
					margin-left: 20rpx;
				}
			}
		}
	}
</style>
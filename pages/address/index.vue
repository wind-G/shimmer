<template>
	<view class="address_content">
		<view class="address_header">
			<view class="ad_head_left"></view>
			<view class="ad_head_right">管理</view>
		</view>
		
		<view class="address_wrap">
			<!-- address_manage -->
			<view class="address_inner">
				<view class="address_item">
					<view class="ad_it_cont">
						<view class="ad_it_avatar">陶</view>
						<view class="ad_it_center">
							<view class="ad_c_hd">
								<view class="ad_c_name">陶某某</view>
								<view class="ad_c_phone">12345678901</view>
								<view class="ad_c_state">默认</view>
							</view>
							<view class="ad_c_text">
								重庆 重庆市 渝中区 石油路街道龙湖时代天街时代汇7号楼2611
							</view>
						</view>
						<view class="ad_it_icon">
							<image src="../../static/icon/del.png" mode=""></image>
						</view>
					</view>
					<view class="ad_it_footer">
						<view class="ad_fr_checkbox">
							<text class="ad_fr_icon"></text>
							默认地址
						</view>
						<view class="ad_fr_del">删除</view>
					</view>
				</view>
				<view class="address_item">
					<view class="ad_it_cont">
						<view class="ad_it_avatar">W</view>
						<view class="ad_it_center">
							<view class="ad_c_hd">
								<view class="ad_c_name">wind</view>
								<view class="ad_c_phone">12345678901</view>
								<!-- <view class="ad_c_state">默认</view> -->
							</view>
							<view class="ad_c_text">
								重庆 重庆市 渝中区 石油路街道龙湖时代天街时代汇7号楼2611
							</view>
						</view>
						<view class="ad_it_icon">
							<image src="../../static/icon/del.png" mode=""></image>
						</view>
					</view>
					<view class="ad_it_footer">
						<view class="ad_fr_checkbox">
							<text class="ad_fr_icon"></text>
							默认地址
						</view>
						<view class="ad_fr_del">删除</view>
					</view>
				</view>
			</view>
		</view>
	
		<!-- kuai -->
		<view class="bulk150"></view>
		<view class="address_button">
			<view class="add_button">+ 添加地址</view>
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
	.address_content{
		.address_header{
			width: 100%;
			display: flex;
			align-items: center;
			padding: 30rpx 30rpx;
			box-sizing: border-box;
			.ad_head_left{
				flex: 1;
			}
			.ad_head_right{
				font-size: 28rpx;
				color: #ff2525;
			}
		}
		.address_wrap{
			width: 100%;
			padding: 0rpx 30rpx;
			box-sizing: border-box;
			.address_inner,
			.address_item{
				width: 100%;
				display: block;
				background-color: #ffffff;
				border-radius: 10rpx;
			}
			.address_manage{
				.address_item{
					margin-top: 20rpx;
				}
			}
			.address_item{
				padding: 0rpx 30rpx;
				box-sizing: border-box;
				.ad_it_cont{
					width: 100%;
					display: flex;
					align-items: center;
					padding: 20rpx 0rpx;
					box-sizing: border-box;
					.ad_it_avatar{
						width: 60rpx;
						height: 60rpx;
						display: flex;
						align-items: center;
						justify-content: center;
						background-color: rgba(251, 31, 120, .2);
						border-radius: 50%;
						font-size: 32rpx;
						color: #f57766;
						font-weight: bold;
					}
					.ad_it_center{
						flex: 1;
						padding: 0rpx 30rpx;
						box-sizing: border-box;
						.ad_c_hd{
							width: 100%;
							display: flex;
							align-items: center;
							.ad_c_name{
								font-size: 26rpx;
								color: #333333;
								font-weight: bold;
							}
							.ad_c_phone{
								margin-left: 10rpx;
								font-size: 22rpx;
								color: #a7a7a7;
							}
							.ad_c_state{
								font-size: 22rpx;
								color: #f57766;
								border: 1px solid #f57766;
								border-radius: 5rpx;
								padding: 2rpx 10rpx;
								box-sizing: border-box;
								margin-left: 10rpx;
							}
						}
						.ad_c_text{
							width: 100%;
							font-size: 26rpx;
							color: #515151;
						}
					}
					.ad_it_icon{
						width: 36rpx;
						height: 36rpx;
						image{
							width: 100%;
							height: 100%;
							display: block;
						}
					}
				}
				.ad_it_footer{
					width: 100%;
					display: flex;
					align-items: center;
					padding: 20rpx 0rpx;
					box-sizing: border-box;
					border-top: 1px solid #f2f2f2;
					.ad_fr_checkbox{
						flex: 1;
						display: flex;
						align-items: center;
						font-size: 24rpx;
						color: #a7a7a7;
						.ad_fr_icon{
							width: 30rpx;
							height: 30rpx;
							border: 1px solid #a7a7a7;
							border-radius: 50%;
							margin-right: 10rpx;
						}
					}
					.ad_fr_del{
						font-size: 26rpx;
						color: #a7a7a7;
					}
				}
			}
		}
		.address_button{
			width: 100%;
			display: block;
			background-color: #ffffff;
			padding: 30rpx 30rpx;
			box-sizing: border-box;
			position: fixed;
			left: 0;
			right: 0;
			bottom: 0;
			z-index: 11;
			.add_button{
				width: 100%;
				height: 80rpx;
				display: flex;
				align-items: center;
				justify-content: center;
				background-color: #f57766;
				box-shadow: 0rpx 6rpx 15rpx #a7a7a7;
				font-size: 36rpx;
				color: #ffffff;
				border-radius: 50rpx;
			}
		}
	}
</style>
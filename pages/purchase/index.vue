<template>
	<view class="purchase_content">
		<view class="purchase_box">
			<view class="pur_commodity marginTop">
				<view class="pur_com_photo">
					<image src="../../static/images/timg.jpg" mode=""></image>
				</view>
				<view class="pur_com_right">
					<view class="pur_com_title">
						接寄拍!!!蹲商家，素人女大学生，时间充裕，可以接各种寄拍，
					</view>
					<view class="pur_com_footer">
						<view class="pur_com_price">￥<text>50.00</text></view>
					</view>
				</view>
			</view>
			<view class="pur_address marginTop">
				<view class="pur_add_cont">
					<view class="pur_add_title">收货地址</view>
					<view class="pur_add_right">
						<view class="pur_add_name">wind12345678900</view>
						<view class="pur_add_text">
							重庆重庆市渝北区龙山街道龙山路72号新城丽都3幢一单元3-3
						</view>
					</view>
				</view>
				<view class="pur_add_bottom">
					<view class="pur_add_title">运送方式</view>
					<view class="pur_add_state">自提</view>
				</view>
			</view>
		</view>
		
		<!--  -->
		<view class="purchase_footer">
			<view class="pur_foot_text">
				<view class="pur_foot_tit">实付款:</view>
				<view class="pur_foot_price">￥<text>50.00</text></view>
			</view>
			<view class="pur_foot_button">确认购买</view>
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
	.purchase_content{
		.purchase_box{
			width: 100%;
			padding: 0rpx 30rpx;
			box-sizing: border-box;
			.pur_commodity{
				width: 100%;
				display: flex;
				background-color: #ffffff;
				padding: 30rpx 30rpx;
				box-sizing: border-box;
				border-radius: 10rpx;
				.pur_com_photo{
					width: 200rpx;
					height: 200rpx;
					border-radius: 10rpx;
					overflow: hidden;
					image{
						width: 100%;
						height: 100%;
						display: block;
					}
				}
				.pur_com_right{
					flex: 1;
					display: flex;
					align-items: stretch;
					flex-direction: column;
					justify-content: space-between;
					flex-wrap: wrap;
					padding-left: 30rpx;
					box-sizing: border-box;
					.pur_com_title{
						width: 100%;
						font-size: 28rpx;
						color: #515151;
						padding-right: 10rpx;
						box-sizing: border-box;
					}
					.pur_com_footer{
						width: 100%;
						text-align: right;
						.pur_com_price{
							font-size: 24rpx;
							color: #ff2525;
							font-weight: bold;
							text{
								font-size: 36rpx;
							}
						}
					}
				}
			}
			.pur_address{
				width: 100%;
				display: block;
				background-color: #ffffff;
				padding: 0rpx 30rpx;
				box-sizing: border-box;
				border-radius: 10rpx;
				.pur_add_title{
					flex: 1;
					font-size: 28rpx;
					color: #515151;
				}
				.pur_add_cont{
					width: 100%;
					display: flex;
					align-items: center;
					padding: 30rpx 0rpx;
					box-sizing: border-box;
					.pur_add_right{
						max-width: 65%;
						text-align: right;
						padding-right: 10rpx;
						box-sizing: border-box;
						.pur_add_name{
							width: 100%;
							font-size: 28rpx;
							color: #333333;
							font-weight: bold;
						}
						.pur_add_text{
							width: 100%;
							font-size: 28rpx;
							color: #a7a7a7;
						}
					}
				}
				.pur_add_bottom{
					width: 100%;
					display: flex;
					align-items: center;
					padding: 30rpx 0rpx;
					box-sizing: border-box;
					border-top: 1px solid #f2f2f2;
					.pur_add_state{
						font-size: 28rpx;
						color: #2878ff;
						font-weight: bold;
					}
				}
			}
		}
		.purchase_footer{
			width: 100%;
			display: flex;
			align-items: center;
			justify-content: flex-end;
			background-color: #ffffff;
			padding: 20rpx 30rpx;
			box-sizing: border-box;
			position: fixed;
			left: 0;
			right: 0;
			bottom: 0;
			z-index: 11;
			.pur_foot_text{
				display: flex;
				align-items: center;
				.pur_foot_tit{
					font-size: 28rpx;
					color: #515151;
				}
				.pur_foot_price{
					font-size: 26rpx;
					font-weight: bold;
					color: #ff2525;
					text{
						font-size: 36rpx;
					}
				}
			}
			.pur_foot_button{
				width: 200rpx;
				height: 80rpx;
				display: flex;
				align-items: center;
				justify-content: center;
				background-image: linear-gradient(to right, #f3db2b,#f54a3a,#ff2525);
				font-size: 32rpx;
				color: #ffffff;
				font-weight: bold;
				border-radius: 50rpx;
				margin-left: 30rpx;
				box-shadow: 5rpx 8rpx 15rpx #a7a7a7;
			}
		}
	}
</style>
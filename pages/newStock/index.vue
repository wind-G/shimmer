<template>
	<view class="life_content">
		<view class="life_box">
			<view class="life_header">
				<view class="life_head_right">
					<view class="life_hd_issue">发布</view>
				</view>
			</view>
			<view class="life_wrap">
				<view class="life_texta">
					<textarea placeholder="怎么样才能让你的微光闪闪发亮~"></textarea>
				</view>
				<view class="life_photo">
					<view class="life_photo_item">
						<view class="life_photo_del">
							<image src="../../static/icon/detele.png" mode=""></image>
						</view>
						<image class="life_ph_img" src="../../static/images/timg.jpg" mode=""></image>
					</view>
					<view class="life_photo_item">
						<view class="life_photo_del">
							<image src="../../static/icon/detele.png" mode=""></image>
						</view>
						<image class="life_ph_img" src="../../static/images/timg.jpg" mode=""></image>
					</view>
					<view class="life_photo_item">
						<view class="life_photo_del">
							<image src="../../static/icon/detele.png" mode=""></image>
						</view>
						<image class="life_ph_img" src="../../static/images/timg.jpg" mode=""></image>
					</view>
					<view class="life_photo_add">
						<image src="../../static/images/phone.png" mode=""></image>
					</view>
				</view>
				
				<!--  -->
				<view class="life_footer">
					<view class="life_ftr_item">
						<image class="le_f_img" src="../../static/icon/price.png" mode=""></image>
						<view class="le_f_tit">价格</view>
						<view class="le_f_cen">
							<view class="le_f_price">￥<text>0.00</text></view>
						</view>
						<image class="le_f_icon" src="../../static/icon/jright.png" mode=""></image>
					</view>
					<view class="life_ftr_item">
						<image class="le_f_img" src="../../static/icon/fahuo.png" mode=""></image>
						<view class="le_f_tit">发货方式</view>
						<view class="le_f_cen">
							<view class="le_f_txt">送货上门</view>
						</view>
						<image class="le_f_icon" src="../../static/icon/jright.png" mode=""></image>
					</view>
				</view>
			</view>
		</view>
		
		<!-- 选择发货方式 -->
		<view class="stock_dialog">
			<ShippingMethod />
		</view>
	</view>
</template>

<script>
	import ShippingMethod from '../../components/shippingMethod/index.vue'
	export default {
		components:{
			ShippingMethod, //选择发货方式弹窗
		},
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
	.life_content{
		.life_box{
			width: 100%;
			height: 100%;
			display: block;
			background-color: #ffffff;
			position: fixed;
			top: 0;
			right: 0;
			left: 0;
			bottom: 0;
		}
		.life_header{
			width: 100%;
			display: flex;
			align-items: center;
			justify-content: flex-end;
			padding: 30rpx 30rpx;
			box-sizing: border-box;
			background-color: #ffffff;
			border-bottom: 1px solid #f2f2f2;
			.life_head_right{
				display: flex;
				align-items: center;
				.life_hd_issue{
					padding: 10rpx 30rpx;
					background-color: #FCCA00;
					border-radius: 50rpx;
					font-size: 30rpx;
					color: #333333;
					font-weight: bold;
				}
			}
		}
		.life_wrap{
			width: 100%;
			display: block;
			padding: 0rpx 30rpx;
			box-sizing: border-box;
			background-color: #ffffff;
			.life_texta{
				width: 100%;
				display: block;
				textarea{
					width: 100%;
					min-height: 300rpx;
					display: block;
					padding: 20rpx 0rpx;
					border: 0;
					outline: none;
					background-color: transparent;
					font-size: 28rpx;
					color: #515151;
				}
			}
			.life_photo{
				width: 100%;
				display: flex;
				flex-wrap: wrap;
				padding-bottom: 30rpx;
				box-sizing: border-box;
				& > view{
					width: 220rpx;
					height: 220rpx;
					background-color: #f2f2f2;
					border-radius: 10rpx;
					overflow: hidden;
					position: relative;
					margin-top: 10rpx;
					margin-right: 10rpx;
				}
				.life_photo_item{
					.life_ph_img{
						width: 100%;
						height: 100%;
						display: block;
					}
					.life_photo_del{
						width: 40rpx;
						height: 40rpx;
						background-color: rgba(0, 0, 0, .5);
						border-radius: 5rpx;
						display: flex;
						align-items: center;
						justify-content: center;
						position: absolute;
						top: 0;
						right: 0;
						z-index: 1;
						image{
							width: 30rpx;
							height: 30rpx;
							display: block;
						}
					}
				}
				.life_photo_add{
					display: flex;
					align-items: center;
					justify-content: center;
					image{
						width: 60rpx;
						height: 60rpx;
					}
				}
			}
			
			// 价格-发货方式
			.life_footer{
				width: 100%;
				border-top: 1px solid #f2f2f2;
				.life_ftr_item{
					width: 100%;
					display: flex;
					align-items: center;
					padding: 30rpx 0rpx;
					box-sizing: border-box;
					.le_f_img{
						width: 50rpx;
						height: 50rpx;
						margin-right: 10rpx;
					}
					.le_f_tit{
						font-size: 28rpx;
						color: #333333;
					}
					.le_f_icon{
						width: 20rpx;
						height: 20rpx;
						margin-left: 10rpx;
					}
					.le_f_cen{
						flex: 1;
						text-align: right;
						.le_f_price{
							font-size: 28rpx;
							color: #ff2525;
							font-weight: bold;
						}
						.le_f_txt{
							font-size: 26rpx;
							color: #a7a7a7;
						}
					}
				}
			}
		}
		
		// 选择发货方式
		.stock_dialog{
			width: 100%;
			height: 100%;
			position: fixed;
			top: 0;
			left: 0;
			right: 0;
			bottom: 0;
			z-index: 11;
			background-color: rgba(0, 0, 0, .5);
		}
	}
</style>
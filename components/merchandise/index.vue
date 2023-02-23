<template>
	<view class="merchandise">
		<view class="merc_type">
			<view class="merc_type_wrap">
				<view class="active">全部 6</view>
				<view>在售 6</view>
				<view>已售出</view>
				<view>剪辑</view>
				<view>剪辑</view>
				<view>剪辑</view>
				<view>剪辑</view>
				<view>剪辑</view>
			</view>
		</view>
		<view class="merc_wrap">
			<view class="merc_wr_left">
				<view class="merc_wr_item">
					<view class="merc_i_photo">
						<image src="../../static/images/timg.jpg" mode="widthFix"></image>
					</view>
					<view class="merc_i_inner">
						<view class="merc_i_title">
							<text>包邮</text>
							软考中级，软件设计师（本人已过）
						</view>
						<view class="merc_i_text">
							<view class="merc_i_price">
								￥<text>50</text>
							</view>
							<view class="merc_i_want">1人想要</view>
						</view>
					</view>
				</view>
			</view>
			<view class="merc_wr_right">
				<view class="merc_wr_item">
					<view class="merc_i_photo">
						<image src="../../static/images/timg2.jpg" mode="widthFix"></image>
					</view>
					<view class="merc_i_inner">
						<view class="merc_i_title">
							<text>配送</text>
							送鲜花，买多了，想送人
						</view>
						<view class="merc_i_text">
							<view class="merc_i_price">
								￥<text>150</text>
							</view>
							<view class="merc_i_want">11人想要</view>
						</view>
					</view>
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

		}
	}
</script>

<style lang="scss" scoped>
	.merchandise{
		.merc_type{
			width: 100%;
			display: block;
			overflow: hidden;
			overflow-x: auto;
			.merc_type_wrap{
				display: block;
				white-space: nowrap;
				view{
					display: inline-block;
					padding: 5rpx 20rpx;
					background-color: #f2f2f2;
					font-size: 24rpx;
					color: #a7a7a7;
					border-radius: 50rpx;
					margin-right: 30rpx;
				}
				.active{
					background-color: #ffCA00;
					color: #333333;
					font-weight: bold;
				}
			}
		}
		.merc_wrap{
			width: 100%;
			display: flex;
			justify-content: space-between;
			.merc_wr_left,
			.merc_wr_right{
				width: 48%;
			}
			.merc_wr_item{
				width: 100%;
				display: block;
				margin-top: 20rpx;
			}
			.merc_i_photo{
				width: 100%;
				position: relative;
				border-radius: 10rpx;
				overflow: hidden;
				image{
					width: 100%;
					display: block;
				}
			}
			.merc_i_inner{
				width: 100%;
				padding: 20rpx 0rpx;
				box-sizing: border-box;
				.merc_i_title{
					width: 100%;
					height: 80rpx;
					font-size: 26rpx;
					color: #333333;
					font-weight: bold;
					overflow: hidden;
					text{
						padding: 0rpx 10rpx;
						position: relative;
						color: #2878ff;
						margin-right: 10rpx;
						&::after{
							content: '';
							width: 1px;
							height: 30rpx;
							display: block;
							background-color: #f2f2f2;
							position: absolute;
							top: 0;
							right: 0;
							bottom: 0;
							margin: auto;
						}
					}
				}
				.merc_i_text{
					width: 100%;
					display: flex;
					align-items: center;
					.merc_i_price{
						font-size: 24rpx;
						color: #ff2525;
						font-weight: bold;
						margin-right: 10rpx;
						text{
							font-size: 32rpx;
						}
					}
					.merc_i_want{
						font-size: 22rpx;
						color: #a7a7a7;
					}
				}
			}
		}
	}
</style>
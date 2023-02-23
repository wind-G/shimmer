<template>
	<view class="collect_cont">
		<view class="collect_item">
			<view class="collect_it_img">
				<image src="../../static/images/timg.jpg" mode=""></image>
			</view>
			<view class="collect_it_right">
				<view class="collect_it_wrap">
					<view class="col_it_title">今日感受夏天温柔的风，我记得我吹过，保持愉悦健康的生活姿态，努力迎接每一天带来的惊喜，加油</view>
					<view class="col_it_center">
						<view class="col_it_price">￥<text>15400</text></view>
						<view class="col_it_text">93人想要</view>
					</view>
				</view>
				<view class="collect_it_ftr">
					<view class="col_ftr_left">
						<view class="col_ftr_img">
							<image src="../../static/images/timg2.jpg" mode=""></image>
						</view>
						<view class="col_ftr_name">奶酪爱吃香菜</view>
					</view>
					<view class="col_ftr_but">我想要</view>
				</view>
			</view>
		</view>
		<view class="collect_item">
			<view class="collect_it_img">
				<image src="../../static/images/timg.jpg" mode=""></image>
			</view>
			<view class="collect_it_right">
				<view class="collect_it_wrap">
					<view class="col_it_title">今日感受夏天温柔的风，我记得我吹过，保持愉悦健康的生活姿态，努力迎接每一天带来的惊喜，加油</view>
					<view class="col_it_center">
						<view class="col_it_price">￥<text>15400</text></view>
						<view class="col_it_text">93人想要</view>
					</view>
				</view>
				<view class="collect_it_ftr">
					<view class="col_ftr_left">
						<view class="col_ftr_img">
							<image src="../../static/images/timg2.jpg" mode=""></image>
						</view>
						<view class="col_ftr_name">奶酪爱吃香菜</view>
					</view>
					<view class="col_ftr_but">我想要</view>
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
	.collect_item{
		width: 100%;
		display: flex;
		align-items: stretch;
		padding: 30rpx 30rpx;
		box-sizing: border-box;
		.collect_it_img{
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
		.collect_it_right{
			flex: 1;
			max-width: 70%;
			padding-left: 20rpx;
			box-sizing: border-box;
			display: flex;
			flex-direction: column;
			justify-content: space-between;
			.collect_it_wrap{
				width: 100%;
				.col_it_title{
					flex: 1;
					width: 100%;
					display: block;
					overflow: hidden;
					text-overflow: ellipsis;
					-o-text-overflow: ellipsis;
					white-space: nowrap;
				}
				.col_it_center{
					width: 100%;
					display: flex;
					align-items: center;
					.col_it_price{
						font-size: 24rpx;
						color: #ff2525;
						font-weight: bold;
						text{
							font-size: 32rpx;
						}
					}
					.col_it_text{
						font-size: 24rpx;
						color: #a7a7a7;
						margin-left: 10rpx;
					}
				}
			}
			.collect_it_ftr{
				width: 100%;
				display: flex;
				align-items: center;
				.col_ftr_left{
					flex: 1;
					display: flex;
					align-items: center;
					.col_ftr_img{
						width: 40rpx;
						height: 40rpx;
						border-radius: 50%;
						overflow: hidden;
						margin-right: 10rpx;
						image{
							width: 100%;
							height: 100%;
							display: block;
						}
					}
					.col_ftr_name{
						font-size: 24rpx;
						color: #a7a7a7;
					}
				}
				.col_ftr_but{
					width: 130rpx;
					height: 60rpx;
					line-height: 60rpx;
					border: 1px solid #e7e7e7;
					border-radius: 50rpx;
					text-align: center;
					font-size: 26rpx;
					color: #333333;
				}
			}
		}
	}
</style>
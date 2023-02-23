<template>
	<view class="estimate_content">
		<view class="estimate_type">
			<view class="active">全部</view>
			<view>好评22</view>
			<view>来自卖家2</view>
			<view>来自买家44</view>
			<view>发货快4</view>
			<view>沟通愉快2</view>
			<view>包装好2</view>
			<view>更多</view>
		</view>
		<view class="estimate_wrap">
			<view class="esti_w_item">
				<view class="esti_it_hd">
					<view class="esti_it_avatar">
						<image src="../../static/logo.png" mode=""></image>
					</view>
					<view class="esti_it_name">
						来自广东的买家
						<text>买家</text>
					</view>
					<view class="esti_it_right">
						好评
					</view>
				</view>
				<view class="esti_it_word">
					不错，发货很快，人很好
				</view>
				<view class="esti_it_footer">
					<view class="esti_it_txt">2023-01-1310:52:24</view>
					<view class="esti_it_txt">广东</view>
				</view>
			</view>
			<view class="esti_w_item">
				<view class="esti_it_hd">
					<view class="esti_it_avatar">
						<image src="../../static/images/timg2.jpg" mode=""></image>
					</view>
					<view class="esti_it_name">
						来自杭州市的买家
						<text>买家</text>
					</view>
					<view class="esti_it_right">
						好评
					</view>
				</view>
				<view class="esti_it_word">
					估吗，最值得信赖的手机寄卖专家，专业数据清除，无需担心数据安全风险，希望您对本次的服务感到满意!
				</view>
				<view class="esti_it_footer">
					<view class="esti_it_txt">2021-12-1505:52:59</view>
					<view class="esti_it_txt">杭州</view>
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
	.estimate_content{
		.estimate_type{
			width: 100%;
			display: flex;
			flex-wrap: wrap;
			align-items: center;
			view{
				width: 220rpx;
				height: 70rpx;
				line-height: 70rpx;
				margin-top: 10rpx;
				margin-right: 10rpx;
				text-align: center;
				border-radius: 10rpx;
				background-color: #f2f2f2;
				font-size: 28rpx;
				color: #515151;
			}
			.active{
				background-color: #ffCA00;
				color: #333333;
				font-weight: bold;
			}
		}
		.estimate_wrap{
			width: 100%;
			padding: 20rpx 0rpx;
			box-sizing: border-box;
			.esti_w_item{
				width: 100%;
				padding: 20rpx 0rpx;
				box-sizing: border-box;
				.esti_it_hd{
					width: 100%;
					display: flex;
					align-items: center;
					.esti_it_avatar{
						width: 60rpx;
						height: 60rpx;
						border-radius: 50%;
						overflow: hidden;
						image{
							width: 100%;
							height: 100%;
							display: block;
						}
					}
					.esti_it_name{
						flex: 1;
						display: flex;
						align-items: center;
						padding: 0rpx 20rpx;
						box-sizing: border-box;
						font-size: 28rpx;
						color: #a7a7a7;
						text{
							background-color: rgba(251, 120, 15, .1);
							font-size: 20rpx;
							color: #f57766;
							padding: 0rpx 10rpx;
							margin-left: 10rpx;
							border-radius: 5rpx;
						}
					}
					.esti_it_right{
						background-color: rgba(251, 120, 15, .1);
						font-size: 20rpx;
						color: #f57766;
						padding: 0rpx 20rpx;
						border-radius: 50rpx;
					}
				}
				.esti_it_word{
					width: 100%;
					font-size: 24rpx;
					color: #515151;
					padding: 10rpx 0rpx;
					box-sizing: border-box;
				}
				.esti_it_footer{
					width: 100%;
					display: flex;
					align-items: center;
					.esti_it_txt{
						font-size: 20rpx;
						color: #a7a7a7;
						margin-right: 10rpx;
					}
				}
			}
		}
	}
</style>
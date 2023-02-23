<template>
	<view class="information">
		<view class="infor_box">
			<view class="infor_wrap">
				<view class="infor_inner">基本信息</view>
				<view class="infor_cont">
					<view class="infor_c_item">
						<view class="infor_c_title">头像</view>
						<view class="infor_c_cen">
							<view class="infor_c_avatar">
								<image src="../../static/images/timg.jpg" mode=""></image>
							</view>
						</view>
						<view class="infor_c_icon">
							<image src="../../static/icon/jright.png" mode=""></image>
						</view>
					</view>
					<view class="infor_c_item">
						<view class="infor_c_title">昵称</view>
						<view class="infor_c_cen">
							<view class="infor_c_text">填写独属昵称，更易被大家记住</view>
						</view>
						<view class="infor_c_icon">
							<image src="../../static/icon/jright.png" mode=""></image>
						</view>
					</view>
					<view class="infor_c_item">
						<view class="infor_c_title">会员名</view>
						<view class="infor_c_cen">
							<view class="infor_c_text">tb83758119</view>
						</view>
						<view class="infor_c_icon">
							<!-- <image src="../../static/icon/jright.png" mode=""></image> -->
						</view>
					</view>
					<view class="infor_c_item">
						<view class="infor_c_title">简介</view>
						<view class="infor_c_cen">
							<view class="infor_c_text">真诚的简介可以让买卖更有信任</view>
						</view>
						<view class="infor_c_icon">
							<image src="../../static/icon/jright.png" mode=""></image>
						</view>
					</view>
					<view class="infor_c_item">
						<view class="infor_c_title">性别</view>
						<view class="infor_c_cen">
							<view class="infor_c_text">选择性别</view>
						</view>
						<view class="infor_c_icon">
							<image src="../../static/icon/jright.png" mode=""></image>
						</view>
					</view>
					<view class="infor_c_item">
						<view class="infor_c_title">生日</view>
						<view class="infor_c_cen">
							<view class="infor_c_text">选择生日</view>
						</view>
						<view class="infor_c_icon">
							<image src="../../static/icon/jright.png" mode=""></image>
						</view>
					</view>
					<view class="infor_c_item">
						<view class="infor_c_title">喜欢的</view>
						<view class="infor_c_cen">
							<view class="infor_c_text">选择喜欢的领域</view>
						</view>
						<view class="infor_c_icon">
							<image src="../../static/icon/jright.png" mode=""></image>
						</view>
					</view>
					<view class="infor_c_item">
						<view class="infor_c_title">院校名称</view>
						<view class="infor_c_cen">
							<view class="infor_c_text">选择院校</view>
						</view>
						<view class="infor_c_icon">
							<image src="../../static/icon/jright.png" mode=""></image>
						</view>
					</view>
					<view class="infor_c_item">
						<view class="infor_c_title">常住地</view>
						<view class="infor_c_cen">
							<view class="infor_c_text">选择你所在的地区</view>
						</view>
						<view class="infor_c_icon">
							<image src="../../static/icon/jright.png" mode=""></image>
						</view>
					</view>
					<view class="infor_c_item">
						<view class="infor_c_title">主页背景</view>
						<view class="infor_c_cen">
							<view class="infor_c_bk">
								<image src="../../static/images/timg.jpg" mode=""></image>
							</view>
						</view>
						<view class="infor_c_icon">
							<image src="../../static/icon/jright.png" mode=""></image>
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
	.information{
		.infor_box{
			width: 100%;
			height: 100%;
			background-color: #ffffff;
			position: fixed;
			top: 0;
			right: 0;
			left: 0;
			bottom: 0;
			z-index: 1;
			.infor_wrap{
				.infor_inner,
				.infor_c_item{
					width:100%;
					padding: 30rpx 30rpx;
					box-sizing: border-box;
				}
				.infor_inner{
					font-size: 24rpx;
					color: #a7a7a7;
					font-weight: bold;
				}
				.infor_c_item{
					display: flex;
					align-items: center;
					.infor_c_title{
						flex: 1;
						font-size: 28rpx;
						color: #333333;
						font-weight: bold;
					}
					.infor_c_cen{
						.infor_c_avatar{
							width: 120rpx;
							height: 120rpx;
							display: block;
							border-radius: 50%;
							overflow: hidden;
							image{
								width: 100%;
								height: 100%;
								display: block;
							}
						}
						.infor_c_text{
							font-size: 28rpx;
							color: #a7a7a7;
						}
						.infor_c_bk{
							width: 150rpx;
							height: 100rpx;
							border-radius: 10rpx;
							overflow: hidden;
							image{
								width: 100%;
								height: 100%;
								display: block;
							}
						}
					}
					.infor_c_icon{
						width: 30rpx;
						height: 30rpx;
						image{
							width: 100%;
							height: 100%;
							display: block;
						}
					}
				}
			}
		}
	}
</style>
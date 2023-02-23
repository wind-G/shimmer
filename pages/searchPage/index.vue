<template>
	<view class="search_content">
		<Search />
		
		<view class="search_box">
			<view class="search_wrap">
				<view class="search_title">
					<view class="sea_tit">历史搜索</view>
					<view class="sea_w_del">
						<image src="../../static/icon/del.png" mode=""></image>
					</view>
				</view>
				<view class="search_type">
					<view @click="searchListClick">蔡司</view>
					<view>古董</view>
					<view>COS</view>
					<view>滑板</view>
					<view>布偶</view>
					<view>旗袍</view>
					<view>洛可可</view>
					<view>黑胶</view>
					<view>珍珠</view>
					<view>Molly</view>
				</view>
			</view>
			<view class="search_wrap">
				<view class="search_title">
					<view class="sea_tit">大家都在玩</view>
				</view>
				<view class="search_type">
					<view>蔡司</view>
					<view>古董</view>
					<view>COS</view>
					<view>滑板</view>
					<view>布偶</view>
					<view>旗袍</view>
					<view>洛可可</view>
					<view>黑胶</view>
					<view>珍珠</view>
					<view>Molly</view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	import Search from '../../components/search/index.vue'
	export default {
		components: {
			Search, // 搜索框
		},
		data() {
			return {
			}
		},
		onLoad() {

		},
		methods: {
			// 点击跳转搜索列表
			searchListClick(){
				uni.navigateTo({
					url: '/pages/searchListPage/index'
				})
			}

		}
	}
</script>

<style lang="scss" scoped>
	.search_content{
		width: 100%;
		height: 100%;
		background-color: #ffffff;
		position: fixed;
		top: 0;
		left: 0;
		right: 0;
		bottom: 0;
		z-index: 1;
		.search_box{
			.search_wrap{
				width: 100%;
				padding: 30rpx 30rpx;
				box-sizing: border-box;
				.search_title{
					width: 100%;
					display: flex;
					align-items: center;
					.sea_tit{
						flex: 1;
						font-size: 28rpx;
						color: #333333;
						font-weight: bold;
					}
					.sea_w_del{
						width: 32rpx;
						height: 32rpx;
						image{
							width: 100%;
							height: 100%;
							display: block;
						}
					}
				}
				.search_type{
					width: 100%;
					display: flex;
					flex-wrap: wrap;
					align-items: center;
					padding: 10rpx 0rpx;
					box-sizing: border-box;
					view{
						padding: 5rpx 20rpx;
						background-color: #f2f2f2;
						border-radius: 50rpx;
						font-size: 24rpx;
						color: #515151;
						margin-top: 10rpx;
						margin-right: 10rpx;
					}
				}
			}
		}
	}
</style>
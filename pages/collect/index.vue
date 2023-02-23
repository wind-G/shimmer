<template>
	<view class="collect_content">
		<!-- kuai -->
		<view class="bulk100"></view>
		
		<view class="collect_type">
			<view class="col_type_wrap">
				<view class="active">全部宝贝 2</view>
				<view>帖子 0</view>
			</view>
		</view>
		
		<!-- list -->
		<view class="collect_list marginTop">
			<CollectList/>
		</view>
	</view>
</template>

<script>
	import CollectList from '../../components/collectList/index.vue'
	export default {
		components:{
			CollectList, //收藏list
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
	.collect_content{
		width: 100%;
		display: block;
		min-height: 100%;
		background-color: #ffffff;
		.collect_type{
			width: 100%;
			padding: 30rpx 30rpx 10rpx;
			box-sizing: border-box;
			white-space: nowrap;
			overflow: hidden;
			position: relative;
			border-bottom: 1px solid #f2f2f2;
			position: fixed;
			top: 0;
			left: 0;
			right: 0;
			z-index: 11;
			.col_type_wrap{
				padding-bottom: 30rpx;
				box-sizing: border-box;
				overflow-y: auto;
				view{
					// width: 100rpx;
					text-align: center;
					display: inline-block;
					font-size: 26rpx;
					color: #a7a7a7;
					position: relative;
					margin-right: 30rpx;
					&::before{
						content: '';
						width: 40rpx;
						height: 8rpx;
						background-color: #FCCA00;
						border-radius: 50rpx;
						display: none;
						position: absolute;
						bottom: -15rpx;
						left: 0;
						right: 0;
						margin: auto;
					}
				}
				.active{
					font-size: 28rpx;
					color: #333333;
					font-weight: bold;
					&::before{
						display: block;
					}
				}
			}
		}
		
		// 收藏
		.collect_list{
		}
	}
</style>
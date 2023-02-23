<template>
	<view class="waterfall_wrap">
		<view class="fall_w_left">
			<view class="fall_w_item" v-for="(item,index) in fallLeftList" :key="item.id" @click="waterfallClick(item)">
				<view class="fall_it_img">
					<image :src="item.imageUrl" alt="" mode="widthFix"></image>
				</view>
				<view class="fall_it_ftr">
					<view class="fall_it_title">{{item.title}}</view>
					<view class="fall_it_price">
						<view class="f_i_price">￥<text>{{item.price}}</text></view>
						<view class="f_i_text" style="color: #A7A7A7;">{{item.text}}</view>
					</view>
					<view class="fall_it_base">
						<view class="f_it_photo">
							<image :src="item.photos" alt="" mode=""></image>
						</view>
						<view class="f_it_name">{{item.name}}</view>
						<view class="f_it_state">
							<text></text>
							{{item.avtive}}
						</view>
					</view>
				</view>
			</view>
		</view>
		<view class="fall_w_right">
			<view class="fall_w_item" v-for="(item,index) in fallRightList" :key="item.id" @click="waterfallClick(item)">
				<view class="fall_it_img">
					<image :src="item.imageUrl" alt="" mode="widthFix"></image>
				</view>
				<view class="fall_it_ftr">
					<view class="fall_it_title">{{item.title}}</view>
					<view class="fall_it_price">
						<view class="f_i_price">￥<text>{{item.price}}</text></view>
						<view class="f_i_text" style="color: #A7A7A7;">{{item.text}}</view>
					</view>
					<view class="fall_it_base">
						<view class="f_it_photo">
							<image :src="item.photos" alt="" mode=""></image>
						</view>
						<view class="f_it_name">{{item.name}}</view>
						<view class="f_it_state">
							<text></text>
							{{item.avtive}}
						</view>
					</view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		props:{
			fallList:Array,
		},
		data() {
			return {
				fallLeftList: [], // 瀑布流数据左
				fallRightList: [], // 瀑布流数据右
				// 初始化左右盒子高度
				leftH:0,
				rightH:0,
			}
		},
		onLoad() {

		},
		created() {
			// 瀑布流数据
			this.fallQuery()
		},
		methods: {
			// 点击跳转详情
			waterfallClick(item){
				uni.navigateTo({
					url:'/pages/productDetails/index'
				})
			},
			// 瀑布流数据
			fallQuery(){
				const that = this;
				console.log('22222')
				that.fallList.forEach(res => {
					uni.getImageInfo({
						src:res.imageUrl,
						success:(image) => {
							// console.log(res)
							// 计算图片渲染高度
							let showH = (50 * image.height) / image.width
							// 判断左右盒子高度
							if(that.leftH <= that.rightH){
								that.fallLeftList.push(res)
								that.leftH += showH
							} else {
								that.fallRightList.push(res)
								that.rightH += showH
							}
						}
					})
				})
			}
		}
	}
</script>

<style lang="scss" scoped>
	.waterfall_wrap{
		display: flex;
		justify-content: space-between;
		.fall_w_left,
		.fall_w_right{
			width: 48%;
		}
		.fall_w_item,
		.fall_it_img{
			width: 100%;
			display: block;
		}
		.fall_w_item{
			margin-top: 20rpx;
		}
		.fall_it_img{
			border-radius: 10rpx;
			overflow: hidden;
			position: relative;
			image{
				width: 100%;
				display: block;
			}
		}
		.fall_it_ftr{
			width: 100%;
			padding: 10rpx 0rpx;
			box-sizing: border-box;
			.fall_it_title{
				max-height: 70rpx;
				width: 100%;
				font-size: 24rpx;
				color: #333333;
				font-weight: bold;
				overflow: hidden;
			}
			.fall_it_price{
				width: 100%;
				margin-top: 10rpx;
				display: flex;
				align-items: center;
				.f_i_price{
					font-size: 20rpx;
					color: #ff2525;
					margin-right: 7rpx;
					text{
						font-size: 28rpx;
						font-weight: bold;
					}
				}
				.f_i_text{
					font-size: 20rpx;
				}
			}
			.fall_it_base{
				width: 100%;
				display: flex;
				align-items: center;
				margin-top: 10rpx;
				.f_it_photo{
					width: 36rpx;
					height: 36rpx;
					border-radius: 50%;
					margin-right: 7rpx;
					overflow: hidden;
					image{
						width: 100%;
						height: 100%;
						display: block;
					}
				}
				.f_it_name{
					flex: 1;
					max-width: 60%;
					font-size: 20rpx;
					color: #A7A7A7;
					overflow: hidden;
					white-space: nowrap;
					text-overflow: ellipsis;
					-o-text-overflow: ellipsis;
				}
				.f_it_state{
					max-width: 60%;
					font-size: 20rpx;
					color: #ff2525;
					background-color: rgba(240, 9, 34, 0.2);
					border-radius: 50rpx;
					padding: 0rpx 10rpx;
					margin-left: 10rpx;
					box-sizing: border-box;
				}
			}
		}
	}
</style>
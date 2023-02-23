<template>
	<view class="method_content">
		<view class="method_footer">
			<view class="method_head">
				选择发货方式
				<image class="met_hd_icon" src="../../static/icon/detele2.png" mode=""></image>
			</view>
			<view class="method_center">
				<view @click="methodTypeClick(1)" :class="typeIndex == 1?'active':''">送货上门</view>
				<view @click="methodTypeClick(2)" :class="typeIndex == 2?'active':''">自提</view>
				<view @click="methodTypeClick(3)" :class="typeIndex == 3?'active':''">配送</view>
			</view>
			<view class="method_input" v-if="typeIndex == 3">
				<text>￥</text>
				<input type="text" placeholder="0.00">
			</view>
			<view class="method_btn">确定</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				typeIndex: null, // 类型选择
			}
		},
		onLoad() {

		},
		methods: {
			// 类型选择
			methodTypeClick(item){
				this.typeIndex = item
			}
		}
	}
</script>

<style lang="scss" scoped>
	.method_content{
		width: 100%;
		height: 100%;
		display: block;
		position: relative;
		.method_footer{
			width: 100%;
			display: block;
			background-color: #ffffff;
			padding: 30rpx 30rpx;
			box-sizing: border-box;
			border-radius: 20rpx 20rpx 0rpx 0rpx;
			position: absolute;
			left: 0;
			right: 0;
			bottom: 0;
			z-index: 1;
			.method_head{
				width: 100%;
				display: block;
				position: relative;
				text-align: center;
				font-size: 36rpx;
				color: #333333;
				.met_hd_icon{
					width: 40rpx;
					height: 40rpx;
					display: block;
					position: absolute;
					top: 5rpx;
					right: 0;
					z-index: 1;
				}
			}
			.method_center{
				width: 100%;
				padding: 20rpx 0rpx;
				box-sizing: border-box;
				display: flex;
				align-items: center;
				justify-content: space-between;
				view{
					width: 30%;
					height: 70rpx;
					line-height: 70rpx;
					text-align: center;
					background-color: #f2f2f2;
					border-radius: 10rpx;
					font-size: 28rpx;
					color: #333333;
				}
				.active{
					background-color: peachpuff;
					color: #ff7766;
				}
			}
			.method_input{
				width: 100%;
				padding: 30rpx 0rpx;
				box-sizing: border-box;
				position: relative;
				text{
					width: 60rpx;
					font-size: 28rpx;
					color: #a7a7a7;
					display: flex;
					align-items: center;
					justify-content: center;
					position: absolute;
					top: 0;
					left: 0;
					bottom: 0;
					z-index: 1;
				}
				input{
					width: 100%;
					height: 70rpx;
					line-height: 70rpx;
					padding: 0rpx 60rpx;
					box-sizing: border-box;
					display: block;
					border: 0;
					outline: none;
					background-color: #f2f2f2;
					border-radius: 50rpx;
					font-size: 28rpx;
					color: #333333;
				}
			}
			.method_btn{
				width: 100%;
				text-align: center;
				height: 80rpx;
				line-height: 80rpx;
				background-color: #FCCf00;
				border-radius: 50rpx;
				font-weight: 30rpx;
				color: #333333;
				font-weight: bold;
			}
		}
	}
</style>
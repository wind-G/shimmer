<template>
	<view class="exchange_box">
		<!-- header -->
		<view class="exchange_head"></view>
		
		<!-- content -->
		<view class="exchange_content">
			<view class="exchange_tab marginTop">
				<view class="ex_tab_wrap">
					<view v-for="(item,index) in exTabList" :key="item.id" :class="item.id == exTabIndex?'active':''" @click="exTabClick(item)">{{item.title}}</view>
				</view>
			</view>
			
			<view class="exchange_ul">
				<ExchangeList :fallList="fallList"/>
			</view>
		</view>
		
		
	</view>
</template>

<script>
	import ExchangeList from '../../../components/exchangeList/index.vue'
	export default {
		components:{
			ExchangeList, // 瀑布流组件
		},
		data() {
			return {
				exTabIndex: 1, // tab下标
				exTabList: [
					{id:1,title:'猜你喜欢'},
					{id:2,title:'运动'},
					{id:3,title:'四坑'},
					{id:4,title:'玩转微光'},
					{id:5,title:'玩转微光'},
					{id:6,title:'玩转微光'},
					{id:7,title:'玩转微光'},
					{id:8,title:'玩转微光'},
					{id:9,title:'数码'},
				],
				
				fallList: [
					{
						id: 1,
						title:'重庆市内，可以提供委托，例如：1、外地不方便回重庆市内，可以提供委托，例如：1、外地不方便回重庆市内，可以提供委托，例如：1、外地不方便回',
						imageUrl: '/static/images/timg2.jpg',
						price:'50',
						text:'9人想要',
						state:1,
						name:'嘟嘟噗噗趴',
						avtive:'特殊玩家',
						photos:'/static/logo.png'
					},
					{
						id: 2,
						title:'外地不方便回',
						imageUrl:'/static/logo.png',
						price:'150',
						text:'19人想要',
						state:1,
						name:'哈哈哈',
						avtive:'特殊玩家',
						photos:'/static/images/timg.jpg'
					},
				], // 瀑布流数据
			}
		},
		onLoad() {

		},
		methods: {
			// tab点击
			exTabClick(item){
				this.exTabIndex = item.id
			}
		}
	}
</script>

<style lang="scss" scoped>
	.exchange_box{
		width: 100%;
		display: block;
		.exchange_content{
			background-color: #ffffff;
			padding-bottom: 30rpx;
		}
		// tab
		.exchange_tab{
			width: 100%;
			padding: 30rpx 30rpx 10rpx;
			box-sizing: border-box;
			white-space: nowrap;
			overflow: hidden;
			position: relative;
			.ex_tab_wrap{
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
		// list
		.exchange_ul{
			width: 100%;
			display: block;
			padding: 0rpx 30rpx;
			box-sizing: border-box;
		}
	}
</style>
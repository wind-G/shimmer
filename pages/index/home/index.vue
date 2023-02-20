<template>
	<view class="empty">
		 <view class="headerTop"></view>
			<!-- header -->
			<view class="home_page_header">
				 <view class="home_header_top">
						 <view class="home_top_code">
							 <image src="../../../static/icon/sign.png" mode=""></image>
							 <text>签到</text>
						 </view>
						 <view class="home_top_title">首页</view>
						 <view class="home_top_xx">
							 <view>
								 <text>0</text>
								 <image src="../../../static/icon/icon-lingdang.png" mode=""></image>
								</view>
							</view>
				 </view>
				 <view class="home_header_cen">
						 <view class="h_search_icon">
							<image src="../../../static/icon/icon-shaoma.png" mode=""></image>
						 </view>
						 <swiper class="search_work" circular vertical :autoplay="autoplay" :interval="interval" :duration="duration">
								<swiper-item>
									<view class="s_work_item">搜索类型1</view>
								</swiper-item>
								<swiper-item>
									<view class="s_work_item">搜索类型2</view>
								</swiper-item>
								<swiper-item>
									<view class="s_work_item">搜索类型3</view>
								</swiper-item>
							</swiper>
						 <view class="search_button">搜索</view>
				 </view>
			</view>
			
			<!-- banner -->
			<view class="home_banner">
				<view class="banner">
					<swiper class="swiper" circular :indicator-dots="indicatorDots" :autoplay="autoplay" :interval="interval" :duration="duration">
						<swiper-item>
							<view class="swiper-item uni-bg-red">A</view>
						</swiper-item>
						<swiper-item>
							<view class="swiper-item uni-bg-green">B</view>
						</swiper-item>
						<swiper-item>
							<view class="swiper-item uni-bg-blue">C</view>
						</swiper-item>
					</swiper>
				</view>
			</view>
			
			<!--  -->
			<view class="home_selection marginTop">
				<view class="home_select_box">
					<view class="home_select_item">
							<view class="home_sel_head"><text class="home_sel_tit">大神作品</text><text class="home_sel_txt">获奖作品</text></view>
							<view class="home_sel_center">
									<view><image src="../../../static/images/list1.jpg"></image></view>
									<view><image src="../../../static/images/timg2.jpg"></image></view>
							</view>
					</view>
					<view class="home_select_item">
							<view class="home_sel_head"><text class="home_sel_tit">直播评比</text><text class="home_sel_txt">作品在线评比</text></view>
							<view class="home_sel_center">
									<view><image src="../../../static/images/banner2.jpg"></image></view>
									<view><image src="../../../static/images/banner3.jpg"></image></view>
							</view>
					</view>
					<view class="home_select_item">
							<view class="home_sel_head"><text class="home_sel_tit">江湖悬赏</text><text class="home_sel_txt">接榜单,赚金贝</text></view>
							<view class="home_sel_center">
									<view><image src="../../../static/images/timg2.jpg"></image></view>
									<view><image src="../../../static/images/timg3.jpg"></image></view>
							</view>
					</view>
					<view class="home_select_item">
							<view class="home_sel_head"><text class="home_sel_tit">一条街</text><text class="home_sel_txt">想买,想卖</text></view>
							<view class="home_sel_center">
									<view><image src="../../../static/images/list1.jpg"></image></view>
									<view><image src="../../../static/images/timg2.jpg"></image></view>
							</view>
					</view>
				</view>
			</view>
			
			<!-- 瀑布流 -->
			<view class="waterfall_count marginTop">
				<view class="waterfall_tab">
					<view class="fall_tab_count">
						<view class="active">猜你喜欢</view>
						<view>最新发布</view>
						<view>晒好物</view>
						<view>晒好物</view>
						<view>晒好物</view>
						<view>晒好物</view>
						<view>晒好物</view>
						<view>晒好物</view>
						<view>晒好物</view>
					</view>
					<view class="fall_tab_add">+</view>
				</view>
				<view class="marginTop">
					<Waterfall :fallList="fallList" />
				</view>
			</view>
			
			<!-- 块 -->
	</view>
</template>

<script>
	import Waterfall from '../../../components/waterfall/index.vue'
	export default {
		components:{
			Waterfall, // 瀑布流商品组件
		},
		data() {
			return {
				indicatorDots: true,
				autoplay: true,
				interval: 2000,
				duration: 200,
				fallList: [
					{
						id: 1,
						title:'重庆市内，可以提供委托，例如：1、外地不方便回',
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
					{
						id: 3,
						title:'重庆市内，可以提供委托，例如：1、外地不方便回',
						imageUrl:'/static/images/timg.jpg',
						price:'10',
						text:'23人想要',
						state:1,
						name:'塔塔它',
						avtive:'特殊玩家',
						photos:'/static/logo.png'
					},
					{
						id: 4,
						title:'重庆市内，可以提供委托，例如：1、外地不方便回',
						imageUrl:'/static/images/timg2.jpg',
						price:'30',
						text:'6人想要',
						state:1,
						name:'丫丫',
						avtive:'特殊玩家',
						photos:'/static/logo.png'
					},
					{
						id: 5,
						title:'北极人来北京办点事，可以随时找我',
						imageUrl:'/static/images/timg2.jpg',
						price:'130',
						text:'61人想要',
						state:1,
						name:'呜呜呜',
						avtive:'玩家',
						photos:'/static/images/timg3.jpg'
					},
					{
						id: 6,
						title:'南京人呢，在滴滴滴滴滴滴滴',
						imageUrl:'/static/images/timg3.jpg',
						price:'30',
						text:'22人想要',
						state:1,
						name:'aads',
						avtive:'特殊玩家',
						photos:'/static/images/list1.jpg'
					}
				], // 瀑布流数据
				
			}
		},
		onLoad() {
			// 刷新页面
			// location.reload()
			console.log('1111')
			// 返回顶部
			uni.pageScrollTo({
				scrollTop:0, // 滚动到顶部距离
				duration:0, // 滚动时长
			})
			
		},
		onShow() {
		},
		methods: {
		}
	}
</script>

<style lang="scss" scoped>
	.empty {}
	
	/*状态栏*/
	.headerTop{
		height: 60rpx;
	}
	.headerTop{background-color:#FCCA00;}
	/*首页*/
	.home_page_header,
	.home_header_cen,
	.home_header_top,
	.home_banner,
	.banner,
	.home_selection{
		width: 100%;
		display: block;
	}
	.home_page_header{
		height: 145rpx;
		padding: 30rpx 30rpx;
		box-sizing: border-box;
		background-color: #FCCA00;
		.home_header_top{
			position: relative;
		}
		.home_top_title{
			width: 80%;
			font-size: 36rpx;
			color: #515151;
			font-weight: bold;
			text-align: center;
			margin: auto;
		}
		.home_top_code,
		.home_top_xx{
			width: 54rpx;
			height: 54rpx;
			display: block;
			position: absolute;
			top: 0;
			bottom: 0;
			margin: auto;
			view,
			image{
				width: 100%;
				height: 100%;
				display: block;
				position: relative;
			}
		}
		.home_top_code{
			left: 30rpx;
			image{
				top: -10rpx;
			}
			text{
				width: 100%;
				text-align: center;
				background-color: #ff2525;
				color: #ffffff;
				font-size: 20rpx;
				border-radius: 50rpx;
				position: absolute;
				bottom: 0;
				left: 0;
				right: 0;
			}
		}
		.home_top_xx{
			right: 30rpx;
			text{
				width: 30rpx;
				height: 30rpx;
				line-height: 30rpx;
				text-align: center;
				background-color: #ff2525;
				border-radius: 50%;
				font-size: 20rpx;
				color: #ffffff;
				display: block;
				position: absolute;
				top: 0;
				right: 0;
				z-index: 1;
			}
		}
		.home_header_cen{
			height: 72rpx;
			line-height: 72rpx;
			background-color: #ffffff;
			border-radius: 50rpx;
			text-align: center;
			position: relative;
			display: flex;
			align-items: center;
			overflow: hidden;
			top: 26rpx;
			// border: 1px solid #ececec;
			box-shadow: 0rpx 10rpx 15rpx #ececec;
			.h_search_icon{
				width: 12%;
				display: flex;
				align-items: center;
				justify-content: center;
				position: relative;
				image{
					width: 46rpx;
					height: 46rpx;
					display: block;
				}
				&::after{
					content:"";
					width: 1px;
					height: 60%;
					display: block;
					background-color:#FCCA00;
					position: absolute;
					top: 0;
					right: 5rpx;
					bottom: 0;
					margin: auto;
				}
			}
			.search_work{
				flex: 1;
				width: 68%;
				height: 100%;
				text-align: left;
				padding-left: 10rpx;
				font-size: 26rpx;
				color: #515151;
				box-sizing: border-box;
			}
			.search_button{
				width: 20%;
				height: 100%;
				background-color:#feac02;
				font-size: 26rpx;
				color: #ffffff;
				font-weight: bold;
			}
		}
	}
	.home_banner{
		padding: 0rpx 30rpx;
		box-sizing: border-box;
		margin-top: 70rpx;
		.banner{
			height: 300rpx;
			border-radius: 10rpx;
			overflow: hidden;
			position: relative;
			background-color: #515151;
			.swiper{
				height: 100%;
			}
		}
		.swiper-item{
			width: 100%;
			height: 100%;
			display: block;
			background-color: #feac02;
		}
	}
	
	.home_selection,
	.home_sectionlist{
		padding: 0rpx 30rpx;
		box-sizing: border-box;
		.home_select_box{
			width: 100%;
			display: flex;
			flex-wrap: wrap;
			background-color: #ffffff;
			border-radius: 15rpx;
			box-shadow: 0rpx 0rpx 15rpx #ececec;
			border:1px solid #ececec;
			text-align: left;
		}
		.home_select_item{
			width: 50%;
			padding: 20rpx 20rpx;
			box-sizing: border-box;
			.home_sel_head{
				display: flex;
				align-items: center;
				.home_sel_tit{
					font-size: 28rpx;
					color: #515151;
					font-weight: bold;
					margin-right: 15rpx;
				}
				.home_sel_txt{
					font-size: 24rpx;
					color: #A7A7A7;
				}
			}
			.home_sel_center{
				margin-top: 20rpx;
				border-radius: 10rpx;
				overflow: hidden;
				display: flex;
				align-items: center;
				view{
					flex: 1;
					width: 50%;
					height: 150rpx;
				}
				image{
					width: 100%;
					height: 100%;
					display: block;
				}
			}
		}
	}
	.waterfall_count{
		width: 100%;
		padding: 0rpx 30rpx;
		box-sizing: border-box;
		.waterfall_tab{
			width: 100%;
			display: block;
			white-space: nowrap;
			overflow: hidden;
			position: relative;
			.fall_tab_count{
				padding-right: 65rpx;
				box-sizing: border-box;
				overflow-y: auto;
				view{
					background-color: #ffffff;
					padding: 10rpx 20rpx;
					box-sizing: border-box;
					border-radius: 50rpx;
					display: inline-block;
					margin-right: 10rpx;
					font-size: 26rpx;
					color: #515151;
				}
				.active{
					background-color: #FCCA00;
					color: #333333;
					font-weight: bold;
				}
			}
			.fall_tab_add{
				width: 60rpx;
				height: 100%;
				display: flex;
				align-items: center;
				justify-content: center;
				font-size: 40rpx;
				color: #333333;
				font-weight: bold;
				background-color: #f2f2f2;
				box-shadow: -10rpx 0rpx 15rpx #f2f2f2;
				position: absolute;
				top: 0;
				right: 0;
				z-index: 1;
			}
		}
		
	}
</style>

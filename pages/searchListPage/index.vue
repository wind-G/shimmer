<template>
	<view class="search_list">
		<Search />
		
		<view class="sr_list_content">
			<!-- type -->
			<view class="sr_list_type">
				<view @click="listClick('All')" :class="listTypeName == 'All'?'active':''">全部</view>
				<view @click="listClick('Exchange')" :class="listTypeName == 'Exchange'?'active':''">操场</view>
				<view @click="listClick('User')" :class="listTypeName == 'User'?'active':''">用户</view>
			</view>
			
			<view class="sr_list_wrap">
				<view class="sr_list_all" v-if="listTypeName == 'All'">
					<view class="list_all_type">
						<view class="active">综合</view>
						<view>价格升序</view>
						<view>最新发布</view>
					</view>
					<view class="list_all_cont">
						<Waterfall :fallList="fallList" />
					</view>
				</view>
				<view class="sr_list_exchange" v-if="listTypeName == 'Exchange'">
					<view class="list_ex_cont">
						<ArticleList />
					</view>
				</view>
				<view class="sr_list_user" v-if="listTypeName == 'User'">
					<view class="list_user_cont">
						<view class="user_cont_item">
							<view class="user_i_avatar">
								<image src="../../static/images/timg3.jpg" mode=""></image>
							</view>
							<view class="user_i_inner">
								<view class="user_i_name">英短三花</view>
								<view class="user_i_text">
									<view>会员名：t***8</view>
									<text>粉丝：0</text>
								</view>
							</view>
						</view>
						<view class="user_cont_item">
							<view class="user_i_avatar">
								<image src="../../static/images/timg2.jpg" mode=""></image>
							</view>
							<view class="user_i_inner">
								<view class="user_i_name">英短</view>
								<view class="user_i_text">
									<view>会员名：t***8</view>
									<text>粉丝：10</text>
								</view>
							</view>
						</view>
						<view class="user_cont_item">
							<view class="user_i_avatar">
								<image src="../../static/images/timg.jpg" mode=""></image>
							</view>
							<view class="user_i_inner">
								<view class="user_i_name">三花</view>
								<view class="user_i_text">
									<view>会员名：t***8</view>
									<text>粉丝：23</text>
								</view>
							</view>
						</view>
					</view>
				</view>
				
			</view>
		</view>
	</view>
</template>

<script>
	import Search from '../../components/search/index.vue'
	import Waterfall from '../../components/waterfall/index.vue'
	import ArticleList from '../../components/articleList/index.vue'
	export default {
		components: {
			Search, // 搜索框
			Waterfall, // 瀑布流商品组件
			ArticleList, // 帖子
		},
		data() {
			return {
				listTypeName:'All',
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

		},
		methods: {
			// 类型切换
			listClick(name){
				this.listTypeName = name
			}

		}
	}
</script>

<style lang="scss" scoped>
	.search_list{
		width: 100%;
		display: block;
		background-color: #ffffff;
		.sr_list_content{
			width: 100%;
			display: block;
			.sr_list_type{
				width: 100%;
				display: flex;
				align-items: center;
				justify-content: space-between;
				view{
					flex: 1;
					text-align: center;
					width: 33%;
					padding: 30rpx 30rpx;
					box-sizing: border-box;
					font-size: 28rpx;
					color: #a7a7a7;
					font-weight: bold;
					position: relative;
				}
				.active{
					color: #333333;
					&::after{
						content: '';
						width: 30rpx;
						height: 6rpx;
						display: block;
						background-color: #FCCA00;
						border-radius: 50rpx;
						position: absolute;
						left: 0;
						right: 0;
						bottom: 10rpx;
						z-index: 1;
						margin: auto;
					}
				}
			}
			.sr_list_wrap{
				width: 100%;
				display: block;
				padding: 0rpx 30rpx;
				box-sizing: border-box;
				.sr_list_all{
					width: 100%;
					padding: 30rpx 0rpx;
					box-sizing: border-box;
					.list_all_type{
						width: 100%;
						display: flex;
						align-items: center;
						justify-content: space-between;
						view{
							padding: 0rpx 20rpx;
							box-sizing: border-box;
							font-size: 24rpx;
							color: #a7a7a7;
						}
						.active{
							font-weight: bold;
							color: #333333;
						}
					}
				}
				.sr_list_exchange{
					width: 100%;
				}
				// 用户
				.sr_list_user{
					width: 100%;
					.user_cont_item{
						width: 100%;
						display: flex;
						align-items: center;
						padding: 20rpx 0rpx;
						box-sizing: border-box;
						.user_i_avatar{
							width: 90rpx;
							height: 90rpx;
							border-radius: 50%;
							overflow: hidden;
							image{
								width: 100%;
								height: 100%;
								display: block;
							}
						}
						.user_i_inner{
							flex: 1;
							padding: 0rpx 30rpx;
							box-sizing: border-box;
							.user_i_name{
								width: 100%;
								display: flex;
								align-items: center;
								font-size: 30rpx;
								color: #333333;
								font-weight: bold;
							}
							.user_i_text{
								width: 100%;
								display: flex;
								align-items: center;
								view{
									margin-right: 10rpx
								}
								view,
								text{
									font-size: 24rpx;
									color: #a7a7a7;
									position: relative;
								}
								text{
									padding: 0rpx 10rpx;
									box-sizing: border-box;
									&::after{
										content: '';
										width: 1px;
										height: 20rpx;
										display: block;
										background-color: #a7a7a7;
										position: absolute;
										top: 0;
										left: 0;
										bottom: 0;
										margin: auto
									}
								}
							}
						}
					}
				}
			}
		}
	}
</style>
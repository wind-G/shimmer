<template>
	<view class="product_box">
		<!--  -->
		<view class="product_header">
			<!-- 个人信息 -->
			<view class="product_info">
				<view class="pro_info_photo">
					<image src="../../static/images/timg.jpg" mode=""></image>
				</view>
				<view class="pro_info_count">
					<view class="pro_info_name">米西米西</view>
					<view class="pro_info_time">
						14小时前来过
						<text class="pro_larg_line"></text>
						南阳
					</view>
				</view>
				<view class="pro_info_button">
					<text>+&nbsp;关注</text>
				</view>
			</view>
			
			<!-- 价格 -->
			<view class="product_price">
				<view class="pro_h_price">￥<text>5.21</text></view>
				<view class="pro_h_largest">
					<text>231人想要</text>
					<text class="pro_larg_line"></text>
					<text>2.4万浏览</text>
				</view>
			</view>
			<!-- 文字 图片 -->
			<view class="product_text">
				<view class="pro_text">
					接寄拍!!!素人女大学生，时间充裕，可以接各种寄拍，衣服，鞋子，化妆品，护肤品，包包，美瞳等等各种产品，按照需求返图，会很用心的拍，有会费的勿扰，本人160.90
				</view>
				<view class="pro_picture">
					<view class="pro_pic" v-for="(img,index) in pictureList" :key="index">
						<image :src="img.src" :mode="index == 0?'widthFix':''"></image>
					</view>
				</view>
				<view class="pro_pict_state">
					<view class="pro_pict_ensure">担保交易</view>
					<view class="pro_pict_del">不喜欢</view>
				</view>
			</view>
		</view>
		
		<!-- 好评率 -->
		<view class="product_reta">
			<view class="pro_reta_count">
				<view class="pro_reta_wrap">
					<view class="pro_reta_item">
						<view class="reta_it_code">卖出</view>
						<view class="reta_it_cont"><text>3</text>笔</view>
						<view class="reta_it_text">发布过8个</view>
					</view>
					<view class="pro_reta_item">
						<view class="reta_it_code">卖出好评</view>
						<view class="reta_it_cont"><text>--</text>条</view>
						<view class="reta_it_text">卖出评价--条</view>
					</view>
					<view class="pro_reta_item">
						<view class="reta_it_code">24小时回复率</view>
						<view class="reta_it_cont">&lt;<text>50</text>%</view>
						<view class="reta_it_text">平均3小时+回复</view>
					</view>
				</view>
			</view>
		</view>
		
		<!-- 留言交流 -->
		<view class="product_message marginTop">
			<view class="pro_msg_title">
				留言<text>75</text>
			</view>
			<view class="msg_interchange">
				<view class="msg_inter_wrap">
					<view class="msg_inter_inner">
						<view class="msg_inter_avatar">
							<image src="../../static/images/timg3.jpg" mode=""></image>
						</view>
						<view class="msg_inter_center">
							<view class="msg_in_hd">
								<view class="msg_in_name">武昌待人</view>
								<view class="msg_in_time">·一个月前</view>
								<view class="msg_in_area">武昌</view>
							</view>
							<view class="msg_in_text">撒大阿达服务大厦的双方各回</view>
						</view>
						<view class="msg_inter_state">
							<image class="msg_inter_btn" src="../../static/tabBar/my2.png" mode=""></image>
						</view>
					</view>
				</view>
				<view class="msg_inter_wrap">
					<view class="msg_inter_inner">
						<view class="msg_inter_avatar">
							<image src="../../static/images/timg2.jpg" mode=""></image>
						</view>
						<view class="msg_inter_center">
							<view class="msg_in_hd">
								<view class="msg_in_name">南京伊人</view>
								<view class="msg_in_time">·1小时前</view>
								<view class="msg_in_area">南京</view>
							</view>
							<view class="msg_in_text">我喜欢你你喜欢我吗？</view>
						</view>
						<view class="msg_inter_state">
							<image class="msg_inter_btn" src="../../static/tabBar/my2.png" mode=""></image>
						</view>
					</view>
				</view>
				
				<view class="msg_inter_all marginTop">
					查看全部留言&nbsp;&RightAngleBracket;
				</view>
			</view>
		</view>
		
		<!-- 为你推荐 -->
		<view class="product_letter marginTop">
			<view class="pro_let_head">
				为你推荐
				<image src="../../static/icon/letter.png" mode=""></image>
			</view>
			<view class="pro_let_cont">
				<Waterfall :fallList="fallList" />
			</view>
		</view>
		
		<!-- kuai -->
		<view style="width: 100%;height: 120rpx;display: block;"></view>
		<!-- nav -->
		<view class="product_footer">
			<view class="pro_footer_box">
				<view class="pro_ftr_type">
					<view class="ftr_type_item">
						<image src="../../static/icon/letter.png" mode=""></image>
						<text>出价</text>
					</view>
					<view class="ftr_type_item">
						<image src="../../static/icon/letter.png" mode=""></image>
						<text>57</text>
					</view>
					<view class="ftr_type_item">
						<image src="../../static/icon/letter.png" mode=""></image>
						<text>51</text>
					</view>
				</view>
				<view class="pro_ftr_but">
					<view class="pro_ftr_sale" @click="stockClick">卖同款</view>
					<view class="pro_ftr_buy" @click="chichatClick">我想要</view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	import Waterfall from '../../components/waterfall/index.vue'
	export default {
		components:{
			Waterfall, // 瀑布流商品组件
		},
		data() {
			return {
				pictureList:[
					{src:'/static/images/timg.jpg'},
					{src:'/static/images/list1.jpg'},
					{src:'/static/images/timg2.jpg'},
					{src:'/static/images/timg3.jpg'},
					{src:'/static/images/banner2.jpg'},
				],
				fallList: [
					{
						id: 1,
						title:'重庆市内，可以提供委托，例如：1、外地不方便回',
						imageUrl: '/static/images/timg2.jpg',
						price:'50',
						text:'9人想要',
						state:1,
						name:'米嘻嘻嘻',
						avtive:'一星',
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
						avtive:'繁星',
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
			// 上架微光
			stockClick(){
				uni.navigateTo({
					url: '/pages/newStock/index'
				})
			},
			// 跳转消息对话
			chichatClick(){
				uni.navigateTo({
					url:'/pages/chitchat/index'
				})
			}
		}
	}
</script>

<style lang="scss" scoped>
	// xian
	.pro_larg_line{
		display: inline-block;
		width: 1px;
		height: 20rpx;
		background-color: #c7c7c7;
		margin: 0rpx 8rpx;
	}
	.product_box{
		.product_header{
			width: 100%;
			display: block;
			background-color: #ffffff;
			padding: 30rpx 30rpx;
			box-sizing: border-box;
			.product_info{
				width: 100%;
				display: flex;
				align-items: center;
				.pro_info_photo{
					width: 70rpx;
					height: 70rpx;
					border-radius: 50%;
					overflow: hidden;
					margin-right: 15rpx;
					image{
						width: 100%;
						height: 100%;
						display: block;
					}
				}
				.pro_info_count{
					flex: 1;
					// max-width: 65%;
					.pro_info_name{
						width: 100%;
						font-size: 28rpx;
						font-weight: bold;
						color: #333333;
					}
					.pro_info_time{
						width: 100%;
						font-size: 20rpx;
						display: flex;
						align-items: center;
						color: #a7a7a7;
					}
				}
				.pro_info_button{
					padding: 10rpx 20rpx;
					background-color: #f2f2f2;
					border-radius: 50rpx;
					font-size: 26rpx;
					color: #333333;
					font-weight: bold;
				}
			}
			.product_price{
				width: 100%;
				display: flex;
				align-items: flex-end;
				padding: 20rpx 0rpx;
				box-sizing: border-box;
				.pro_h_price{
					flex: 1;
					font-size: 24rpx;
					color: #ff2525;
					font-weight: bold;
					text{
						font-size: 46rpx;
					}
				}
				.pro_h_largest{
					display: flex;
					align-items: center;
					font-size: 20rpx;
					color: #a7a7a7;
				}
			}
			.product_text{
				width: 100%;
				.pro_text{
					width: 100%;
					display: block;
					font-size: 28rpx;
				}
				.pro_picture{
					width: 100%;
					border-radius: 10rpx;
					display: flex;
					flex-wrap: wrap;
					justify-content: space-between;
					overflow: hidden;
					margin-top: 30rpx;
					image{
						width:100%;
						height: 100%;
						display: block;
					}
					.pro_pic{
						width: 49.8%;
						height: 350rpx;
						margin-top: 1px;
					}
					.pro_pic:first-child{
						width: 100%;
						height: auto;
					}
				}
				.pro_pict_state{
					width: 100%;
					padding-top: 30rpx;
					display: flex;
					align-items: center;
					view{
						font-size: 24rpx;
					}
					.pro_pict_ensure,{
						flex: 1;
						color: #03a8fe;
					}
					.pro_pict_del{
						color: #a7a7a7;
					}
				}
			}
		}
		// 好评率
		.product_reta{
			width: 100%;
			display: block;
			background-color: #ffffff;
			padding: 30rpx 30rpx;
			box-sizing: border-box;
			margin-top: 1px;
			.pro_reta_count{
				width: 100%;
				background-color: #f2f2f2;
				border-radius: 10rpx;
				position: relative;
				.pro_reta_wrap{
					width: 100%;
					display: flex;
					align-items: center;
					justify-content: space-between;
					.pro_reta_item{
						width: 33.3%;
						position: relative;
						padding: 20rpx 20rpx;
						box-sizing: border-box;
						&::before{
							content: '';
							width: 1px;
							height: 100rpx;
							background-color: #e7e7e7;
							display: block;
							position: absolute;
							top: 0;
							left: 0;
							bottom: 0;
							margin: auto;
						}
						.reta_it_code{
							font-size: 24rpx;
							color: #666666;
						}
						.reta_it_cont{
							font-size: 24rpx;
							color: #333333;
							text{
								font-size: 40rpx;
								font-weight: bold;
							}
						}
						.reta_it_text{
							font-size: 20rpx;
							color: #a7a7a7;
						}
					}
					.pro_reta_item:first-child{
						&::before{
							width: 0px;
						}
					}
				}
			}
		}
		
		// 留言交流
		.product_message{
			width: 100%;
			display: block;
			background-color: #ffffff;
			padding: 30rpx 30rpx;
			box-sizing: border-box;
			.pro_msg_title{
				font-size: 32rpx;
				color: #333333;
				font-weight: bold;
				text{
					margin-left: 10rpx;
				}
			}
			.msg_interchange{
				width: 100%;
				display: block;
				.msg_inter_wrap{
					width: 100%;
					margin-top: 30rpx;
					.msg_inter_inner{
						width: 100%;
						display: flex;
						align-items: center;
						.msg_inter_avatar{
							width: 60rpx;
							height: 60rpx;
							border-radius: 50%;
							overflow: hidden;
							margin-right: 20rpx;
							image{
								width: 100%;
								height: 100%;
								display: block;
							}
						}
						.msg_inter_center{
							flex: 1;
							.msg_in_hd{
								width: 100%;
								display: flex;
								align-items: center;
								.msg_in_name{
									font-size: 28rpx;
									color: #666666;
									font-weight: bold;
								}
								.msg_in_time{
									font-size: 20rpx;
									color: #a7a7a7;
								}
								.msg_in_area{
									background-color: #f2f2f2;
									font-size: 20rpx;
									color: #a7a7a7;
									border-radius: 3rpx;
									padding: 0rpx 10rpx;
									box-sizing: border-box;
									margin-left: 10rpx;
								}
							}
							.msg_in_text{
								width: 100%;
								display: block;
								font-size: 26rpx;
								color: #333333;
								margin-top: 10rpx;
							}
						}
						.msg_inter_state{
							.msg_inter_btn{
								width: 40rpx;
								height: 40rpx;
								display: block;
							}
						}
					}
				}
				.msg_inter_all{
					width: 100%;
					text-align: center;
					font-size: 28rpx;
					color: #a7a7a7;
					font-weight: bold;
				}
			}
		}
		
		// 为你推荐
		.product_letter{
			width: 100%;
			background-color: #ffffff;
			padding: 30rpx 30rpx;
			box-sizing: border-box;
			.pro_let_head{
				width: 100%;
				font-size: 32rpx;
				color: #333333;
				font-weight: bold;
				display: flex;
				align-items: center;
				justify-content: center;
				image{
					width: 46rpx;
					height: 46rpx;
					display: inline-block;
					margin-left: 10rpx;
				}
			}
			.pro_let_cont{
				width: 100%;
			}
		}
		
		// nav
		.product_footer{
			width: 100%;
			background-color: #ffffff;
			border-top: 1px solid #eeeeee;
			padding: 20rpx 30rpx;
			box-sizing: border-box;
			position: fixed;
			left: 0;
			right: 0;
			bottom: 0;
			z-index: 11;
			.pro_footer_box{
				width: 100%;
				display: flex;
				align-items: center;
				.pro_ftr_type{
					flex: 1;
					display: flex;
					align-items: center;
					.ftr_type_item{
						margin-left: 40rpx;
						image{
							width: 46rpx;
							height: 46rpx;
							display: block;
							margin: auto;
						}
						text{
							display: block;
							text-align: center;
							font-size: 22rpx;
							color: #a7a7a7;
						}
					}
					.ftr_type_item:first-child{
						margin-left: 0rpx;
					}
				}
				.pro_ftr_but{
					display: flex;
					align-items: center;
					view{
						width: 170rpx;
						height: 70rpx;
						display: flex;
						align-items: center;
						justify-content: center;
						margin-left: 20rpx;
						border-radius: 50rpx;
						font-size: 32rpx;
					}
					.pro_ftr_sale{
						background-color: #f2f2f2;
						color: #515151;
					}
					.pro_ftr_buy{
						background-color: #f57766;
						color: #ffffff;
						font-weight: bold;
					}
				}
			}
		}
	}
</style>
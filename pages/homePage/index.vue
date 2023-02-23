<template>
	<view class="home_page">
		<view class="main_header">
			<image class="main_head_img" src="../../static/images/timg.jpg" mode=""></image>
			<view class="main_bk_bottom"></view>
		</view>
		<view class="main_info_box">
			<view class="main_info">
				<view class="main_info_avatar">
					<image src="../../static/images/timg3.jpg" mode=""></image>
				</view>
				<view class="main_info_cont">
					<view class="main_info_name">小范饭啾咪啾咪</view>
					<view class="main_info_time">2小时前来过微光</view>
				</view>
			</view>
			<view class="main_score">
				<view class="main_s_pink">百分好评</view>
			</view>
			<view class="main_intro">
				<view class="main_io_text">
					这个人很神秘，什么也没有留下，没有写下个人简介没有写下个人简介没有写下个人简介没有写下个人简介
				</view>
				<view class="main_io_more" @click="infoMoreClick">更多</view>
			</view>
		</view>
		
		<!--  -->
		<view class="main_type">
			<view class="main_type_cont">
				<view class="main_type_left">
					<view><text>5</text>关注</view>
					<view><text>7</text>粉丝</view>
				</view>
				<view class="main_type_right">
					<view class="main_t_att">+ &nbsp;关注</view>
					<view class="main_t_edit">编辑资料</view>
				</view>
			</view>
		</view>
		
		<view class="main_merchandise">
			<view class="main_merch_type">
				<view class="merch_t_item" @click="merchType('Merchandise')" :class="merchTypeName == 'Merchandise'?'active':''">微光<text>12</text></view>
				<view class="merch_t_item" @click="merchType('ArticleList')" :class="merchTypeName == 'ArticleList'?'active':''">帖子<text>0</text></view>
				<view class="merch_t_item" @click="merchType('Estimate')" :class="merchTypeName == 'Estimate'?'active':''">评价<text>4</text></view>
				<view class="merch_t_item" @click="merchType('Dynamic')" :class="merchTypeName == 'Dynamic'?'active':''">动态<text>26</text></view>
			</view>
			
			<view class="merch_content">
				<Merchandise v-if="merchTypeName == 'Merchandise'" />
				<ArticleList v-if="merchTypeName == 'ArticleList'" />
				<Estimate v-if="merchTypeName == 'Estimate'" />
				<Dynamic v-if="merchTypeName == 'Dynamic'" />
			</view>
		</view>
		
	</view>
</template>

<script>
	import Merchandise from '../../components/merchandise/index.vue'
	import ArticleList from '../../components/articleList/index.vue'
	import Estimate from '../../components/estimate/index.vue'
	import Dynamic from '../../components/dynamic/index.vue'
	export default {
		components: {
			Merchandise, // 微光商品
			ArticleList, // 帖子
			Estimate, // 评价
			Dynamic, // 动态
		},
		data() {
			return {
				merchTypeName: 'Merchandise'
			}
		},
		onLoad() {

		},
		methods: {
			// type切换
			merchType(name){
				this.merchTypeName = name
			},
			// 更多
			infoMoreClick(){
				console.log('更多')
			}
		}
	}
</script>

<style lang="scss" scoped>
	.home_page{
		.main_header{
			width: 100%;
			height: 300rpx;
			display: block;
			position: relative;
			.main_head_img{
				width: 100%;
				height: 100%;
				display: block;
			}
			.main_bk_bottom{
				width: 100%;
				height: 100rpx;
				display: block;
				background-image: linear-gradient(to bottom,transparent,rgba(0,0,0,.5));
				position: absolute;
				left: 0;
				right: 0;
				bottom: 0;
				z-index: 1;
			}
		}
		.main_info_box{
			background-color: #ffffff;
			padding: 0rpx 30rpx;
			box-sizing: border-box;
			.main_info{
				width: 100%;
				height: 130rpx;
				display: flex;
				align-items: flex-end;
				padding: 20rpx 0rpx;
				box-sizing: border-box;
				position: relative;
				z-index: 2;
				.main_info_avatar{
					width: 150rpx;
					height: 150rpx;
					border-radius: 50%;
					border: 10rpx solid #ffffff;
					overflow: hidden;
					image{
						width: 100%;
						height: 100%;
						display: block;
					}
				}
				.main_info_cont{
					flex: 1;
					padding-left: 20rpx;
					box-sizing: border-box;
					.main_info_name{
						width: 100%;
						font-size: 34rpx;
						color: #333333;
						font-weight: bold;
					}
					.main_info_time{
						width: 100%;
						font-size: 24rpx;
						color: #a7a7a7;
					}
				}
			}
			.main_score{
				width: 100%;
				display: flex;
				align-items: center;
				padding: 10rpx 0rpx;
				box-sizing: border-box;
				view{
					padding: 0rpx 10rpx;
					border-radius: 50rpx;
					font-size: 24rpx;
					font-weight: bold;
					margin-right: 10rpx;
				}
				.main_s_pink{
					background-color: rgba(251,20,130,.1);
					color: #f57766;
				}
			}
			.main_intro{
				width: 100%;
				display: block;
				position: relative;
				padding-bottom: 20rpx;
				box-sizing: border-box;
				.main_io_text{
					width: 100%;
					padding-right: 60rpx;
					box-sizing: border-box;
					font-size: 26rpx;
					color: #515151;
				}
				.main_io_more{
					font-size: 26rpx;
					color: #515151;
					position: absolute;
					top: 0;
					right: 0;
					z-index: 1;
				}
			}
		}
		.main_type{
			width: 100%;
			padding: 0rpx 30rpx;
			box-sizing: border-box;
			background-color: #ffffff;
			.main_type_cont{
				width: 100%;
				display: flex;
				align-items: center;
				border-bottom: 1px solid #f2f2f2;
				padding: 30rpx 0rpx;
				box-sizing: border-box;
				.main_type_left{
					flex: 1;
					display: flex;
					align-items: center;
					view{
						font-size: 24rpx;
						color: #515151;
						margin-right: 20rpx;
						text{
							font-size: 30rpx;
							color: #333333;
							font-weight: bold;
							margin-right: 10rpx;
						}
					}
				}
				.main_type_right{
					display: flex;
					align-items: center;
					view{
						width: 180rpx;
						height: 70rpx;
						line-height: 70rpx;
						text-align: center;
						border-radius: 50rpx;
						font-size: 30rpx;
						color: #333333;
						font-weight: bold;
					}
					.main_t_att{
						background-color: #FCCA00;
					}
					.main_t_edit{
						background-color: #f2f2f2;
					}
				}
			}
		}
		.main_merchandise{
			width: 100%;
			background-color: #ffffff;
			.main_merch_type{
				width: 100%;
				display: flex;
				padding: 30rpx 30rpx;
				box-sizing: border-box;
				.merch_t_item{
					font-size: 30rpx;
					color: #515151;
					margin-right: 60rpx;
					position: relative;
					text{
						font-size: 20rpx;
						position: absolute;
						top: 0;
						left: 110%;
						z-index: 1;
					}
				}
				.active{
					color: #333333;
					font-weight: bold;
					&::before{
						content: '';
						width: 40rpx;
						height: 6rpx;
						display: block;
						background-color: #FCCA00;
						border-radius: 50rpx;
						position: absolute;
						bottom: -10rpx;
						left: 0;
						right: 0;
						margin: auto;
					}
				}
			}
			.merch_content{
				width: 100%;
				padding: 0rpx 30rpx 30rpx;
				box-sizing: border-box;
			}
		}
	}
</style>
<template>
	<view class="helang-tab-content">
		<view class="helang-tab-bar">
			<view class="placeholder"></view>
			<view class="bar">
				<view class="bulgy" :style="bulgyMove"></view>
				<view class="h-flex-x h-flex-5">
					<view class="item h-flex-x h-flex-center"
						v-for="(item,index) in  tabList" 
						:key="index" 
						:class="{
							'active':current == index,
							'recover':prevIndex == index
						}"
						@tap="change(index, item)"
					>
						<view>
							<view class="h-flex-x h-flex-center">
								<view class="icon">
									<!-- <view class="iconfont" :class="item.icon" style="font-size: 48rpx;"></view> -->
									<!-- <img class="icon-img" :src="current == index ? item.selectedIconPath : item.iconPath" alt="" srcset=""> -->
									<image class="icon-img" :src="current == index ? item.selectedIconPath : item.iconPath" alt="" mode=""></image>
									
								</view>
							</view>
							<view class="h-flex-x h-flex-center">
								{{item.text}}
							</view>
						</view>
					</view>
				</view>
				
			</view>
		</view>
		<!-- kuai -->
		<view class="helang-block"></view>
	</view>
</template>

<script>
	
	export default {
		// 冒泡
		name:"tabBar",
		components: {
		},
		props:{
			// 固定底部
			tabList:{
				type:Array,
				default:true
			}
		},
		data() {
			return {
				prevIndex:-1,
				current:0
			};
		},
		computed:{
			bulgyMove(){
				let style = `left:${this.current/this.tabList.length*100}%`;
				return style;
			}
		},
		methods:{
			change(index, row){
				if(this.current == index)return;
				// this.prevIndex = this.current;
				this.current = index;
				// console.log("打开到应用的某个页面", index)
				this.$emit('tabChange', index);
			}
		}
	}
</script>

<style lang="scss" scoped>
@import "@/style/helang-flex.scss";
@import "@/style/tab-bar.scss";
.helang-tab-content{
	width: 100%;
	display: block;
}
.helang-block{
	width: 100%;
	height: 160rpx;
	display: block;
}
.helang-tab-bar{
	width: 100%;
	position: fixed;
	left: 0;
	right: 0;
	bottom: 0;
	z-index: 99;
	.bar{
		background-color: #ffffff;
	}
	
	// 凸起
	.bulgy{
		width: 20%;
		height: 60rpx;
		overflow: hidden;
		position: absolute;
		left: 0;
		top: -38rpx;
		transition: left 0.2s ease 0s;
		z-index: 0;
		&:before{
			content: '';
			display: block;
			width: 300rpx;
			height: 600rpx;
			border-radius: 50%;
			background-color: #ffffff;
			position: absolute;
			top: 0;
			left: 50%;
			margin-left: -150rpx;
			z-index: 1;
		}
	}
	
	.item{
		height: 100rpx;
		position: relative;
		color: #333333;
		font-size: 22rpx;
		line-height: normal;
		
		.icon-img{
			width: 48rpx;
			height: 48rpx;
			display: block;
			margin: auto;
		}
		
		&.active{
			animation:font 0.2s ease 0.1s 1 normal;
			animation-fill-mode:forwards;
			
			.icon{
				position: relative;
				animation:translate 0.2s ease 0.1s 1 normal;
				animation-fill-mode:forwards;
				
				/deep/ .iconfont{
					color: #24a7c5 !important;
				}
				
				&::before{
					content: '';
					display: block;
					position: absolute;
					top: 0;
					left: 0;
					width: 100%;
					height: 100%;
					z-index: -1;
					opacity: 0;
					border-radius: 50%;
					animation:scale 0.3s ease 0.2s 1 normal;
					animation-fill-mode:forwards;
				}
			}
			
			
		}
		
		&.recover{
			.icon{
				animation:recover 0.3s ease 0s 1 normal;
			}
		}
	}
}

// 恢复默认
@keyframes recover
{
	from {
		transform:translateY(-20rpx) scale(1.1,1.1);
	}
	to {
		transform:translateY(0) scale(1,1);
	}
}
// 转换移动
@keyframes translate
{
	from {
		transform:translateY(0) scale(1,1);
	}
	to {
		transform:translateY(-20rpx) scale(1.1,1.1);
	}
}
// 圆圈缩放
@keyframes scale
{
	0% {
		transform:scale(1,1);
		opacity: 0;
		background-color: #fe8003;
	}
	100% {
		transform:scale(1.5,1.5);
		opacity: 0.22;
		background-color: #fe8003;
	}
}

// 淡入
@keyframes font
{
	from {
		color: #f57766;
	}
	to {
		color: #f57766;
	}
}
</style>

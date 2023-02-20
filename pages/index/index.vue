<template>
	<view class="content">
		<view>
			<template>
				<Home v-if="tabName === 'home'"></Home>
				<Exchange v-else-if="tabName === 'exchange'"></Exchange>
				<SellThings v-else-if="tabName === 'sellThings'"></SellThings>
				<Meet v-else-if="tabName === 'meet'"></Meet>
				<Personal v-else-if="tabName === 'personal'"></Personal>
			</template>
		</view>
		
		<!-- 底部导航 -->
		<tab-bar :tabList="tabList" @tabChange="tabChange"></tab-bar>
	</view>
</template>

<script>
	import Home from './home/index.vue'
	import Exchange from './exchange/index.vue'
	import SellThings from './sellThings/index.vue'
	import Meet from './meet/index.vue'
	import Personal from './personal/index.vue'
	
	import tabBar from "@/components/tabBar/index.vue";
	export default {
		components: {
			Home, // 首页
			Exchange, //操场
			SellThings, // 出售微光
			Meet, // 消息
			Personal, // 个人中心
			"tab-bar": tabBar,
		},
		data() {
			return {
				tabList:[
					{
						"name": "home",
						"icon":"icon-shouyefill",
						"iconPath": "../../static/tabBar/home2.png",
						"selectedIconPath": "../../static/tabBar/home1.png",
						"text":"首页",
						"url": "/page/index/home/index" 
					},
					{
						"name": "exchange",
						"icon":"icon-a-Frame20",
						"iconPath": "../../static/tabBar/exchange2.png",
						"selectedIconPath": "../../static/tabBar/exchange1.png",
						"text":"操场",
						"url": "/page/index/exchange/index" 
					},
					{
						"name": "sellThings",
						"icon":"icon-jingcaishike",
						"iconPath": "../../static/tabBar/sellThings2.png",
						"selectedIconPath": "../../static/tabBar/sellThings1.png",
						"text":"出售微光",
						"url": "/page/index/sellThings/index" 
					},
					{
						"name": "meet",
						"icon":"icon-shouye3",
						"iconPath": "../../static/tabBar/meet2.png",
						"selectedIconPath": "../../static/tabBar/meet1.png",
						"text":"消息",
						"url": "/page/index/meet/index" 
					},
					{
						"name": "personal",
						"icon":"icon--xingxingtuijian",
						"iconPath": "../../static/tabBar/personal2.png",
						"selectedIconPath": "../../static/tabBar/personal1.png",
						"text":"我的",
						"url": "/page/index/personal/index" 
					},
				],
				tabName: 'home'
			}
		},
		onLoad() {
		},
		onShow() {
			
		},
		methods: {
			// tab点击
			tabChange(index){
				// console.log('tab点击', index)
				this.tabName = this.tabList[index].name
			},

		}
	}
</script>

<style lang="scss" scoped>
	.content {
		/* display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center; */
	}

	.logo {
		height: 200rpx;
		width: 200rpx;
		margin-top: 200rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}

	.text-area {
		display: flex;
		justify-content: center;
	}

	.title {
		font-size: 36rpx;
		color: #8f8f94;
	}
</style>

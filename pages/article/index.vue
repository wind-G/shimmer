<template>
	<view class="article_content">
		<ArticleList/>
	</view>
</template>

<script>
	import ArticleList from '../../components/articleList/index.vue'
	export default {
		components: {
			ArticleList, // 帖子组件
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
	.article_content{
		
	}
</style>
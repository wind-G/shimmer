<script>
	export default {
		onLaunch: function() {
			console.log('App Launch')
		},
		onShow: function() {
			console.log('App Show')
		},
		onHide: function() {
			console.log('App Hide')
		}
	}
</script>

<style>
	/*每个页面公共css */
	page{
		background-color: #f2f2f2;
	}
	/*  */
	.marginTop{
		margin-top: 30rpx;
	}
	/* 块-填充物 */
	.bulk150{
		width: 100%;
		height: 150rpx;
		display: block;
	}
	.bulk100{
		width: 100%;
		height: 100rpx;
		display: block;
	}
	.bulk{
		width: 100%;
		height: 150rpx;
		display: block;
	}
</style>

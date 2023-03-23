<script>
	export default {
		data(){
			return{
				
			}
		},
		onLaunch: function() {
			console.log('App Launch')
		},
		onShow: function() {
			console.log('App Show')
		},
		onHide: function() {
			console.log('App Hide')
		},
		globalData:{
			height:'100vh',
			compatibleHeight(){
				const type = uni.getSystemInfoSync().uniPlatform
				if(type == 'web'){
					this.height = 'calc(100vh - 209rpx)';
					console.log(this.height)
				}
			}
		}
	}
</script>

<style lang="scss">
	@import "uview-ui/index.scss";
	/*每个页面公共css */
</style>

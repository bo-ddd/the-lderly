<script>
	export default {
		data() {
			return {

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
		globalData: {
			height: '100vh',
			compatibleHeight(num) {
				const type = uni.getSystemInfoSync().uniPlatform;
				if (num == 1) {
					if (type == 'web') {
						this.height = 'calc(100vh - 209rpx)';
					}
				} else if (num == 2) {

					if (type == 'web') {
						this.height = 'calc(100vh - 88rpx)';
					}
				}
			}
		}
	}
</script>

<style lang="scss">
	@import "uview-ui/index.scss";
	/*每个页面公共css */
</style>

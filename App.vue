<script>
	export default {
		data() {
			return {

			}
		},
		methods: {
			compatibleHeight(num) {
				const type = uni.getSystemInfoSync().uniPlatform;
				let h = '100vh';
				if (num == 1) {
					if (type == 'web') {
						h = 'calc(100vh - 200rpx)';
					}
				} else if (num == 2) {

					if (type == 'web') {
						h = 'calc(100vh - 88rpx)';
					}
				}
				return h
			}
		},
		onLaunch: function() {
			console.log('App Launch')
		},
		onShow: function() {
			uni.hideTabBar();
			console.log('App Show')
		},
		onHide: function() {
			console.log('App Hide')
		},
		globalData: {

		}
	}
</script>

<style lang="scss">
	@import "uview-ui/index.scss";

	/*每个页面公共css */
	.flex-center {
		display: flex;
		align-items: center;
		justify-content: center;
	}

	.align-center {
		display: flex;
		align-items: center;
	}

	.space-around {
		display: flex;
		align-items: center;
		justify-content: space-around;
	}
</style>

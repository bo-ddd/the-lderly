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
			},
			getHeaderHeight(){
				let viewType = uni.getSystemInfoSync().uniPlatform; //设备类型
				let statusHeight = uni.getSystemInfoSync().statusBarHeight; //状态栏高度
				let headHight;
				if (viewType == 'mp-weixin') {
					console.log('wx')
					let cachetPosition = wx.getMenuButtonBoundingClientRect(); //微信小程序胶囊信息
					headHight = statusHeight + (cachetPosition.top - statusHeight) * 2 + cachetPosition.height;
					console.log(cachetPosition)
					this.globalData.headHeight = headHight * 2;
					this.globalData.paddingTop = statusHeight * 2;
				} else if (viewType == 'app') {
					console.log('app')
					this.globalData.headHeight = 130;
					this.globalData.paddingTop = statusHeight * 2;
				}
			}	
		},
		onLaunch: function() {
			console.log('App Launch')
			this.getHeaderHeight();
			console.log(this)
		},
		onShow: function() {
			uni.hideTabBar();
			console.log('App Show')
		},
		onHide: function() {
			console.log('App Hide')
		},
		globalData: {
			headHeight:'',
			paddingTop:''
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

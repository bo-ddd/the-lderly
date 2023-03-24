<template>
	<view v-if="showselected"
	   <view class="tabbar">
			<view class="navigator">
				<view class="navigator-item" v-for="(item,index) in tabBar.list" :key="item.pagePath"
					@click="switchTab(index,item)">
						<img :src="item.iconPath" class="icon" v-if="selectedIndex !== index">
						<img :src="item.selectedIconPath" class="icon" v-else>
						<text :class="['item-text',{'text-active':selectedIndex === index}]">{{item.text}}</text>
				</view> 
			</view>
		</view>
	  </view>
</template>

<script>
	export default {
		watch: {
					$route: {
						immediate: true,
						handler(to) {
							console.log(to)
							if (to) {
								// this.__path__ = this.$route.path
								this.showselected = true
								const index = this.tabBar.list.findIndex(item => to.meta.pagePath === item.pagePath)
								if (index > -1) {
									this.selectedIndex = index
								}
							}
						}
					}
				},
		data() {
			return {
				selectedIndex: 0, // 标记
				showselected: false, // 是否在页面使用tarBar
				tabBar: {
					list: [{
							"pagePath": "pages/home/home",
							"iconPath": "static/images/icon-farm.png",
							"selectedIconPath": "static/images/icon-farm-selected.png",
							"text": "首页"
						}, {
							"pagePath": "pages/mine/mine",
							"iconPath": "static/images/icon-mine.png",
							"selectedIconPath": "static/images/icon-mine-selected.png",
							"text": "我的"
						}
					]
				}
			}
		},
		methods: {
			switchTab(index, item) {

						 let _this =  this
							let url = '/' + item.pagePath
							let pagePath = url
							const detail = {
							  index,
							  pagePath
							}
							if (_this.$route.path !== url) {
								console.log(_this.$route.path)
							  // this.__path__ = this.$route.path
							  uni.switchTab({
							    from: 'tabBar',
							    url,
							    detail
							  })
							} else {
							  // UniServiceJSBridge.emit('onTabItemTap', detail)
							}
							_this.selectedIndex = index
							// this.$emit('switchTab', detail)
						}
		}
	}
</script>

<style>
.tabbar {
		position: fixed;
		bottom: 0;
		left: 0;
		width: 100%;
		height: 100rpx;
		z-index: 999;
		background: #F5F5F5;
		border-top: 2rpx solid #eee;
	}
 
	.navigator {
		display: flex;
		justify-content: space-around;
		gap: 100rpx;
		width: 85%;
		margin: 0 auto;
		padding: 20rpx;
	}
 
	.navigator-item {
		display: flex;
		align-items: center;
		flex-direction: column;
		width: 50rpx;
		height: 100%;
	}
 
	.item-text {
		margin-top: 6rpx;
		color: #777E86;
		font-size: 24rpx;
	}
 
	.text-active {
		color: #3ec247 !important;
	}
 
	.icon {
		width: 20px;
		height: 20px;
	}
</style>

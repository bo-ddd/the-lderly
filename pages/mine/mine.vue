<template>
	<view class="content" :style="{'height':height}">
		
		<view class="title">
			我 的
		</view>
		
			<scroll-view  scroll-y="true" class="scroll-Y my-content warp" >
			<view class="user-info">
				<view class="head-box">
					<image class="head" src="../../static/logo.png" mode=""></image>
				</view>
				<view class="info">
					<view>Sun</view>
					<view>绑定手机: 未绑定</view>
					<view>id: 182976381792</view>
				</view>
			</view>
			
			<view class="banner">
				<image src="../../static/images/mine-banner.png" mode=""></image>
			</view>
			
			<view class="help-list" v-for="item in helpList">
				<view class="list-left">
					<image class="list-icon" :src="item.listIcon" mode=""></image>
					<view class="list-title">
						{{ item.listTitle }}
					</view>
				</view>
				<image class="list-arrowhead" :src="item.listArrowhead" mode=""></image>
			</view>
			
				</scroll-view>
		
	</view>
</template>

<script>
	export default {
		data() {
			return {
				height:'100vh',
				scrollTop: 0,
				old: {
				scrollTop: 0
				},
				helpList:[
					{
						id:1,
						listIcon:'../../static/images/icon-rule.png',
						listArrowhead:'../../static/images/icon-arrowhead-right.png',
						listTitle:'游戏规则'
					},
					{
						id:2,
						listIcon:'../../static/images/icon-customer-service.png',
						listArrowhead:'../../static/images/icon-arrowhead-right.png',
						listTitle:'帮助中心'
					},
					{
						id:3,
						listIcon:'../../static/images/icon-set-up.png',
						listArrowhead:'../../static/images/icon-arrowhead-right.png',
						listTitle:'游戏设置'
					},
				]
			}
		},
		created(){
			getApp().globalData.compatibleHeight();
			this.height = getApp().globalData.height;
		},
		methods: {
			
		}
	}
</script>

<style lang="scss">
	
	view,text{
		margin: 0;
		padding: 0;
	}
	.warp{
		width: 650rpx;
		margin: 0 auto;
	}
.content{
	height: 100vh;

	background: url("@/static/images/mine.background.png") no-repeat;
	background-size:cover;
}
.title{
	height: 120rpx;
	color: #fcea62;
	display: flex;
	align-items: center;
	justify-content: center;
	font-size: 40rpx;
	font-weight: 700;
}
.my-content{
	padding: 30rpx 20rpx;
	margin-top: 50rpx;
	background-color: #f3e4b9;
	border-radius: 20rpx;
}
.head-box{
	display: flex;
	justify-content: center;
	align-items: center;
	border-radius: 20rpx;
	width: 115rpx;
	height: 115rpx;
	background-color: #edad2f;
	filter: drop-shadow(4rpx 4rpx rgba(149,64,25,.5));
}
.head{
	width: 100rpx;
	height: 100rpx;
	border-radius: 20rpx;
}
.user-info{
	display: flex;
	align-items: center;
}
.info{
	margin-left: 30rpx;
	font-weight: 700;
	color: #8b6d47;
}
.banner{
	margin-top: 40rpx;
}
.banner image{
	width: 100%;
	height: 250rpx;
	border-radius: 20rpx;
}
.help-list{
	margin-top: 20rpx;
	border: 2px solid #72452e;
	border-radius: 20rpx;
	padding: 30rpx;
	display: flex;
	align-items: center;
	justify-content: space-between;
}
.list-icon{
	width: 80rpx;
	height: 80rpx;
}
.list-arrowhead{
	width: 40rpx;
	height: 40rpx;
}
.list-title{
	margin-left: 40rpx;
	font-weight: 700;
	color: #743c2f;
}
.list-left{
	display: flex;
	align-items: center;
}
// scroll
.scroll-Y {
			height: 80%;
		}

</style>

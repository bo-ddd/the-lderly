<template>
	<view class="page-box">
		<view class="box wrap">
			<view class="title">
				余额详情
			</view>
			<view class="content-box">
				<image src="" mode=""></image>
				<view class="brown-text">
					我的余额
				</view>
				<view class="money-text">
					0.00元
				</view>
			</view>
			<view class="content-box">
				<view class="title">
					提现金额
				</view>
				<view class="select-box">
					<view class="item">
						20元
					</view>
					<view class="item">
						100元
					</view>
					<view class="item">
						500元
					</view>
					<view class="item">
						2000元
					</view>
					<view class="item">
						5000元
					</view>
					<view class="item">
						10000元
					</view>
				</view>
				<view class="link-box">
					<view class="item">
						<view class="left-text">
							兑换到：<image src="" mode=""></image>
						</view>
						<view class="right-icon">
							未实名<image src="" mode=""></image>
						</view>
					</view>
					<view class="item">
						<view class="left-text">
							兑换到：<image src="" mode=""></image>
						</view>
						<view class="right-icon">
							未实名<image src="" mode=""></image>
						</view>
					</view>
					<view class="item">
						<view class="left-text">
							兑换到：<image src="" mode=""></image>
						</view>
						<view class="right-icon">
							未实名<image src="" mode=""></image>
						</view>
					</view>
				</view>
				<view class="tip-box red-text">
					每日可提现1次，提现申请后1个工作日内到账，到账金额扣除3%手续费。
				</view>
				<view class="submit-btn">
					提现
				</view>
			</view>
		</view>
	</view>
</template>

<script>
</script>

<style scoped lang="scss">
.page-box{
	// background-image: url('../../static/images/img-woodback.png');
	.box{
	background-image: url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAASUAAABrCAYAAAAxQpTfAAAACXBIWXMAAC4jAAAuIwF4pT92AAAF8WlUWHRYTUw6Y29tLmFkb2JlLnhtcAAAAAAAPD94cGFja2V0IGJlZ2luPSLvu78iIGlkPSJXNU0wTXBDZWhpSHpyZVN6TlRjemtjOWQiPz4gPHg6eG1wbWV0YSB4bWxuczp4PSJhZG9iZTpuczptZXRhLyIgeDp4bXB0az0iQWRvYmUgWE1QIENvcmUgNi4wLWMwMDIgNzkuMTY0NDg4LCAyMDIwLzA3LzEwLTIyOjA2OjUzICAgICAgICAiPiA8cmRmOlJERiB4bWxuczpyZGY9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkvMDIvMjItcmRmLXN5bnRheC1ucyMiPiA8cmRmOkRlc2NyaXB0aW9uIHJkZjphYm91dD0iIiB4bWxuczp4bXA9Imh0dHA6Ly9ucy5hZG9iZS5jb20veGFwLzEuMC8iIHhtbG5zOmRjPSJodHRwOi8vcHVybC5vcmcvZGMvZWxlbWVudHMvMS4xLyIgeG1sbnM6cGhvdG9zaG9wPSJodHRwOi8vbnMuYWRvYmUuY29tL3Bob3Rvc2hvcC8xLjAvIiB4bWxuczp4bXBNTT0iaHR0cDovL25zLmFkb2JlLmNvbS94YXAvMS4wL21tLyIgeG1sbnM6c3RFdnQ9Imh0dHA6Ly9ucy5hZG9iZS5jb20veGFwLzEuMC9zVHlwZS9SZXNvdXJjZUV2ZW50IyIgeG1wOkNyZWF0b3JUb29sPSJBZG9iZSBQaG90b3Nob3AgMjIuMCAoV2luZG93cykiIHhtcDpDcmVhdGVEYXRlPSIyMDIzLTAzLTIyVDE3OjQxOjM5KzA4OjAwIiB4bXA6TW9kaWZ5RGF0ZT0iMjAyMy0wMy0yMlQxNzo0OTo0NCswODowMCIgeG1wOk1ldGFkYXRhRGF0ZT0iMjAyMy0wMy0yMlQxNzo0OTo0NCswODowMCIgZGM6Zm9ybWF0PSJpbWFnZS9wbmciIHBob3Rvc2hvcDpDb2xvck1vZGU9IjMiIHBob3Rvc2hvcDpJQ0NQcm9maWxlPSJzUkdCIElFQzYxOTY2LTIuMSIgeG1wTU06SW5zdGFuY2VJRD0ieG1wLmlpZDpkYzZmN2M0Mi0xNjMzLTMwNDItYTczZi01MDcwMTcwNzg4M2EiIHhtcE1NOkRvY3VtZW50SUQ9ImFkb2JlOmRvY2lkOnBob3Rvc2hvcDpiMjA4ZTIzZi1lODc1LTMzNDctYmIzZC0xNmRlYjkzNTg0ZjciIHhtcE1NOk9yaWdpbmFsRG9jdW1lbnRJRD0ieG1wLmRpZDpiMTIwMThjOC01MzQ0LTJjNGEtOGU3My0yMjkwNmMzMDc2OGMiPiA8eG1wTU06SGlzdG9yeT4gPHJkZjpTZXE+IDxyZGY6bGkgc3RFdnQ6YWN0aW9uPSJjcmVhdGVkIiBzdEV2dDppbnN0YW5jZUlEPSJ4bXAuaWlkOmIxMjAxOGM4LTUzNDQtMmM0YS04ZTczLTIyOTA2YzMwNzY4YyIgc3RFdnQ6d2hlbj0iMjAyMy0wMy0yMlQxNzo0MTozOSswODowMCIgc3RFdnQ6c29mdHdhcmVBZ2VudD0iQWRvYmUgUGhvdG9zaG9wIDIyLjAgKFdpbmRvd3MpIi8+IDxyZGY6bGkgc3RFdnQ6YWN0aW9uPSJzYXZlZCIgc3RFdnQ6aW5zdGFuY2VJRD0ieG1wLmlpZDpkYzZmN2M0Mi0xNjMzLTMwNDItYTczZi01MDcwMTcwNzg4M2EiIHN0RXZ0OndoZW49IjIwMjMtMDMtMjJUMTc6NDk6NDQrMDg6MDAiIHN0RXZ0OnNvZnR3YXJlQWdlbnQ9IkFkb2JlIFBob3Rvc2hvcCAyMi4wIChXaW5kb3dzKSIgc3RFdnQ6Y2hhbmdlZD0iLyIvPiA8L3JkZjpTZXE+IDwveG1wTU06SGlzdG9yeT');
	}
}
.wrap{
	width:710rpx;
	margin: 0 auto;
}
.title{
	
}
.brown-text{
	color: #252612;
}
.m-y-10{
	margin: 10rpx 0;
}
</style>

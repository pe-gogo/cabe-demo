<template>
	<view class="container">
	
		<view class="banner">
			<image  style="height: 600rpx;width: 100%;" src="../../../static/chiji.jpg"></image>
		</view>			
		<view class="b-index">
			<view class="content">
				<view class="item" @tap="takeIn()">
					<image class="b-images" style="height: 60rpx;width: 60rpx;" src="../../../static/eat.png"></image>
					<view class="title">点餐</view>
				</view>
				
				<view class="item" @tap="takeOut()">
					<image class="b-images" src="../../../static/toC.png" style="height: 60rpx;width: 60rpx;"></image>
					<view class="title">外送</view>
				</view>
			</view>
		</view>
		
	</view>
</template>

<script>
	export default {
		data() {
			return {
					list: [{
									image: 'https://cdn.uviewui.com/uview/swiper/1.jpg',
									title: '昨夜星辰昨夜风，画楼西畔桂堂东'
								},
								{
									image: 'https://cdn.uviewui.com/uview/swiper/2.jpg',
									title: '身无彩凤双飞翼，心有灵犀一点通'
								},
								{
									image: 'https://cdn.uviewui.com/uview/swiper/3.jpg',
									title: '谁念西风独自凉，萧萧黄叶闭疏窗，沉思往事立残阳'
								}
							],
						}	
		},
		methods: {
			takeIn(){console.log("吃饭")},
			takeOut(){console.log("外送")}
		}
	}
</script>

<style lang="scss">
	.container {
		background-color: #F1F8FA;
		height: auto;			
		min-height: 100%;
		
		.banner{
			width: 100%;
		}
		.b-index{
			padding:  0 30px ;
			.content{
					position: relative;
					display: flex;
					flex-direction: row;
					margin-top:-80rpx ;
					margin-bottom: 30px;
					border-radius: 10px;	
					background-color: rebeccapurple;
					padding:  0 30px ;
					background-color: #ffffff;
					.item{
						flex: 1;
						display: flex;
						flex-direction: column;
						justify-content: center;
						align-items: center;
						position: relative;
						&:nth-child(1):after {
							content: '';
							position: absolute;
							width: 1rpx;
							background-color: #ddd;
							right: 0;
							height: 100%;
							transform: scaleX(0.5) scaleY(0.8);
						}
						.b-images{
							width: 84rpx;
							height: 84rpx;
							margin: 20rpx;
						}
						.title {
							font-size: 30rpx;
							color: lightblue;
							font-weight: 600;
						}
					}
				}
			}
		}
		
</style>

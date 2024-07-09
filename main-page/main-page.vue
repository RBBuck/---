<template>
	<view class="body">
		
		<view class="headbk">
		<view class="head-1">
			<input id="mytext" type="text" name="" placeholder="搜索服务/事项">
		</view>
		<view class="head-2">
				<view class="tools-item">
					<image src="@/static/icon/扫码.png" mode="widthFix"></image>
					<view>扫一扫</view>
				</view>
				<view class="tools-item">
					<image src="@/static/icon/二维码.png" mode="widthFix"></image>
					<view>随申码</view>
				</view>
				<view class="tools-item">
					<image src="@/static/icon/身份证.png" mode="widthFix"></image>
					<view>亮证</view>
				</view>
				<view class="tools-item">
					<image src="@/static/icon/耳机.png" mode="widthFix"></image>
					<view>客服</view>
				</view>
				<view class="tools-item">
					<image src="@/static/icon/皇冠.png" mode="widthFix"></image>
					<view>专属</view>
				</view>
		</view>
		<h1 style="padding-left: 30rpx;">晚上好!</h1>
		</view>
		
		
		<view class="head-3">
			<view class="tools-item">
				<image src="@/static/icon/沪惠保.png" mode="widthFix"></image>
				<view>沪惠保</view>
			</view>
			<view class="tools-item">
				<image src="@/static/icon/三金账单.png" mode="widthFix"></image>
				<view>三金账单</view>
			</view>
			<view class="tools-item">
				<image src="@/static/icon/居住证办理.png" mode="widthFix"></image>
				<view>居住证办理</view>
			</view>
			<view class="tools-item">
				<image src="@/static/icon/红途.png" mode="widthFix"></image>
				<view>红途</view>
			</view>
			<view class="tools-item">
				<image src="@/static/icon/爱心暑托班.png" mode="widthFix"></image>
				<view>爱心暑托班</view>
			</view>
			<view class="tools-item">
				<image src="@/static/icon/出入境.png" mode="widthFix"></image>
				<view>出入境</view>
			</view>
			<view class="tools-item">
				<image src="@/static/icon/快处易赔.png" mode="widthFix"></image>
				<view>快处易赔</view>
			</view>
			<view class="tools-item">
				<image src="@/static/icon/上海之夏国_.png" mode="widthFix"></image>
				<view>上海之夏国...</view>
			</view>
		</view>
		
		<view class="banner">
			<swiper :indicator-dots="true"
			        :autoplay="true"
					indicator-color="rgba(255,255,255,.5)"
					indicator-active-color="#ffffff"
					:interval="3000"
					:duration="500">
			<!-- </view> -->
			<swiper-item v-for="(item,index) in swiper" :key="index">
				<view class="item">
					<image :src="item.src" class="img"></image>
				</view>
			</swiper-item>
			</swiper>
		</view>
		
		<view class="zhuti">
			<h1 style="padding-left: 30rpx;">精选主题</h1>
			<view class="zhuti1">
				<scroll-view class="scroll-view" scroll-x>
					<view class="item" v-for="(item,index) in recommendlists" :key="index">
							<image class="img" :src="item.picUrl"></image>
					</view>	
				</scroll-view>
			</view>
			
			<view class="banner">
				<swiper :indicator-dots="true"
				        :autoplay="true"
						indicator-color="rgba(255,255,255,.5)"
						indicator-active-color="#ffffff"
						:interval="3000"
						:duration="500">
				<!-- </view> -->
				<swiper-item v-for="(item,index) in swiper2" :key="index">
					<view class="item">
						<image :src="item.srcs" class="img"></image>
					</view>
				</swiper-item>
				</swiper>
			</view>
			
		</view>
		
		<view class="daohanglan">
		<!-- 	/static/icon/daohang1.jpg
			/static/icon/daohang2.jpg
			/static/icon/daohang3.jpg -->
			<view class="segmented-control">
								<uni-segmented-control :current="current" :values="items" @clickItem="onClickItem" styleType="button">
								</uni-segmented-control>
			</view>
			<uni-list>
				<uni-list-item title="高温天天见!上海发布高温橙色预警" note="2024-07-08&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;上海发布"
									thumb="/static/icon/daohang1.jpg"
									thumb-size="lg" />
				<uni-list-item title="沪2024年中考、初二历史学业考成绩下周公布!查询方式在此" note="2024-07-08&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;上海发布"
														thumb="/static/icon/daohang2.jpg"
														thumb-size="lg" />
				<uni-list-item title="松江、崇明这些公交线路将临时调整" note="2024-07-08&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;上海发布"
								thumb="/static/icon/daohang3.jpg"
								thumb-size="lg"/>
			</uni-list>
			
		</view>
		
		<view class="list-wrap">
			
		<view class="list-scroll-view">
			
			
			
			
			</view>
		</view>
		<view class="tools">
			<view class="tools-item">
				<image src="@/static/icon/首页.png" mode="widthFix"></image>
				<view>首页</view>
			</view>
			<view class="tools-item">
				<image src="@/static/icon/书签.png" mode="widthFix"></image>
				<view>办事</view>
			</view>
			<view class="tools-item">
				<image src="../static/icon/眼睛.png" mode="widthFix"></image>
				<view>发现</view>
			</view>
			<view class="tools-item">
				<image src="../static/icon/保佑.png" mode="widthFix"></image>
				<view>互动</view>
			</view>
			<view class="tools-item">
				<image src="../static/icon/头像.png" mode="widthFix"></image>
				<view>我的</view>
			</view>
		</view>
		
	</view>
</template>

<script>
	export default {
		data() {                                 
			return {
				swiper:[
					{id:1,src:'/static/icon/20241.jpg'},
					{id:2,src:'/static/icon/20242.jpg'},
					{id:3,src:'/static/icon/20243.jpg'},
					{id:4,src:'/static/icon/20244.jpg'},
					{id:5,src:'/static/icon/20245.jpg'},
					{id:6,src:'/static/icon/20246.jpg'},
					{id:7,src:'/static/icon/20247.jpg'},
					{id:8,src:'/static/icon/20248.jpg'},
					{id:9,src:'/static/icon/20249.jpg'},
					{id:10,src:'/static/icon/202410.jpg'},
					{id:11,src:'/static/icon/202411.jpg'},
					{id:12,src:'/static/icon/202412.jpg'}
				],
				recommendlists:[
					{id:1,picUrl:'/static/icon/zhuti1.jpg'},
					{id:2,picUrl:'/static/icon/zhuti2.jpg'},
					{id:3,picUrl:'/static/icon/zhuti3.jpg'},
					{id:4,picUrl:'/static/icon/zhuti4.jpg'},
					{id:5,picUrl:'/static/icon/zhuti5.jpg'},
					{id:6,picUrl:'/static/icon/zhuti6.jpg'},
					{id:7,picUrl:'/static/icon/zhuti7.jpg'},
					{id:8,picUrl:'/static/icon/zhuti8.jpg'},
					{id:9,picUrl:'/static/icon/zhuti9.jpg'},
					{id:10,picUrl:'/static/icon/zhuti10.jpg'}
				],
				swiper2:[
					{id:1,srcs:'/static/icon/zhengce1.jpg'},
					{id:2,srcs:'/static/icon/zhengce2.jpg'},
					{id:3,srcs:'/static/icon/zhengce3.jpg'}
				],
				// list: [{
				// 			name: '待收货'
				// 	    }, {
				// 			name: '待付款'
				// 		}, {
				// 			name: '待评价'
				// 		}],
				current: 0,
				items: ['热点关注', '政策图解'],
			}
		}
		
		}
</script>

<style lang="scss">
	.headbk{
		background: url("@/static/icon/wh860.jpg");
		background-repeat: no-repeat;
		background-size: 100%;
	}
	.body{
		display: flex;
		flex-direction: column;
	}
	.head-2{
		display: flex;
		flex-direction:row;
		justify-content: space-between;
	}
	.head-3{
		display: flex;
		flex-direction:row;
		justify-content: space-between;
		flex-wrap: wrap;
	}
	.banner{
		width: 400px;
		height: 150px;
		// display: flex;
	}
	.list-wrap{
		/* position: relative; */
	}
	.list-scroll-view{
		/* position: absolute;
		top:0;
		left:0;
		right: 0;
		bottom: 0; */
		display: flex;
		flex-direction: row;
		flex-wrap: wrap;
		justify-content: space-between;
		margin-left: 2vw;
		margin-right: 2vw;
	}
	.course-card{
		width:47vw;
		margin-top:10px;
		margin-bottom: 10px;
	}
	.course-card image{
		width:100%;
		border-radius: 5px;
	}
	.tools{
		display: flex;
		flex-direction:row;
		justify-content: space-between;
	}
	.tools-item{
		width:45px;
		text-align:center;
		font-size:14px;
		padding:20px;
	}
	.tools-item image{
		width:24px;
	}
	.zhuti1{
		
	}
	.zhuti1 image{
		width:100px;
		height:120px;
	}
	.scroll-view{
		width: 100%;
		  // background-color: gray;
		  height: 240rpx;
		  white-space: nowrap;
	}
	
	
	.scroll-view .item{
		// background-color: greenyellow;
		  height: 220rpx;
		  width: 200rpx;
		  margin-top: 10rpx;
		  margin-bottom: 10rpx;
		  margin-left: 10rpx;
		  
		  display: inline-block;
	}
	
	
	
	
	// dddd
	page {
				color: #1a1a1a;
				font-size: 24rpx;
			}
			
			.banner {
				width: 100%;
				height: 268rpx;
				margin: 30rpx auto 44rpx;
				.swiper{
					height: 268rpx;
				}
				.item{
					position:relative;
					display: block;
					width: 686rpx;
					height: 268rpx;
					margin: 0 auto;
					border-radius: 14rpx;
					overflow: hidden;
				}
				.img {
					display: block;
					width: 100%;
					height: 100%;
				}
				
			}
		
</style>

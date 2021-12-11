<template>
	<view>
	<view><uni-search-bar bgColor="#efeeef" placeholder = "股票搜索" @confirm="search" @input="input" ></uni-search-bar></view>
	<view>
	<uni-grid :column="3" :showBorder="false"  :square="false" >
    <uni-grid-item >
		<view class="fangxing">
        <p class="text">上证指数</p>
		</view>
    </uni-grid-item>
    <uni-grid-item>
		<view class="fangxing">
        <p class="text">啊啊啊</p>
		</view>
    </uni-grid-item>
    <uni-grid-item>
		<view class="fangxing">
       <p class="text">上证指数</p>
	   </view>
    </uni-grid-item>
	</uni-grid>
	</view>
	<view class="gupiaopaihang"><text style="word-spacing: 50px;">股票排行</text></view>
	<uni-table border stripe emptyText="暂无更多数据" >
	    <!-- 表头行 -->
	    <uni-tr>
	        <uni-th align="center" width="50rpx">股票名称</uni-th>
	        <uni-th align="center" width="30rpx">最新价</uni-th>
	        <uni-th align="left">涨跌幅</uni-th>
			<uni-th align="left">涨速</uni-th>
	    </uni-tr>
	    <!-- 表格数据行 -->
	    <uni-tr v-for="item in stocks">
	        <uni-td>{{item.name}}</uni-td>
	        <uni-td>{{item.newp}}</uni-td>
	        <uni-td>{{item.updown}}</uni-td>
			<uni-td>{{item.upspd}}</uni-td>
	    </uni-tr>
	</uni-table>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: '贝塔科技',
				stocks:[
				// {name:'1',newp:'1',updown:'1',upspd:'1'},
				// {name:'2',newp:'2',updown:'2',upspd:'2'}
				]
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.logo {
		height: 200rpx;
		width: 200rpx;
		margin-top: 200rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}

	.text-area {
		display: flex;
		justify-content: center;
	}
	.title {
		font-size: 36rpx;
		color: #8f8f94;
	}
	.uni-form-item{
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}
	.fangxing{
		background-color: #DD524D;
		width:200rpx;
		height: 200rpx;
		margin: auto;
		border-radius:25rpx;
		text-align: center;
		
	}
	.text{
		font:sans-serif;
		color: #F1F1F1;
		padding-top: 30rpx;
		
	}
	.gupiaopaihang
	{
		font-size: large;
		font-weight: bold;
		padding-left: 50rpx;
		margin-top: 30rpx;
		margin-bottom: 30rpx;
		
	}
</style>

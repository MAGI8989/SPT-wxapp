<template>
	<view class="content">
		<div id="ad" >
		</div>
		<div id="main">
			<div id="styles">
				<!-- 侧边菜品分类 -->
				<tui-list-view>
					<div v-for="item in styles" :key="item.id" style="color: #fafafa;background-color: #202326;text-align: center;margin-top: 100rpx;">
						<tui-list-cell :hover="true" :arrow="false">{{item.text}}</tui-list-cell>
					</div>
				</tui-list-view>
			</div>
			<div class="dishes" style="float: right;">
				<!-- 主体菜单 -->
				<tui-fab :btnList="btnList" :left="90" :right="0" :maskClosable=true >
				</tui-fab>
			</div>
		</div>
		<div id="bill">
			
		</div>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				styles:[
					{text:"进店必买"},
					{text:"特色凉菜"},
					{text:"爆炒荤菜"},
					{text:"小炒素材"},
					{text:"营养汤品"},
					{text:"香辣套餐"},
					{text:"主食"}
				],
				dishes:[
					{name:"xxx",picture:"static/xiangjianxiaopai.jpg",price:88.88,tips:["ttt","ttt"],detail:"xxx"},
					{name:"xxx",picture:"static/xiangjianxiaopai.jpg",price:88.88,tips:["ttt","ttt"],detail:"xxx"},
					{name:"xxx",picture:"static/xiangjianxiaopai.jpg",price:88.88,tips:["ttt","ttt"],detail:"xxx"},
					{name:"xxx",picture:"static/xiangjianxiaopai.jpg",price:88.88,tips:["ttt","ttt"],detail:"xxx"},
					{name:"xxx",picture:"static/xiangjianxiaopai.jpg",price:88.88,tips:["ttt","ttt"],detail:"xxx"},
					{name:"xxx",picture:"static/xiangjianxiaopai.jpg",price:88.88,tips:["ttt","ttt"],detail:"xxx"},
					{name:"xxx",picture:"static/xiangjianxiaopai.jpg",price:88.88,tips:["ttt","ttt"],detail:"xxx"},
					{name:"xxx",picture:"static/xiangjianxiaopai.jpg",price:88.88,tips:["ttt","ttt"],detail:"xxx"},
					{name:"xxx",picture:"static/xiangjianxiaopai.jpg",price:88.88,tips:["ttt","ttt"],detail:"xxx"},
					{name:"xxx",picture:"static/xiangjianxiaopai.jpg",price:88.88,tips:["ttt","ttt"],detail:"xxx"},
					{name:"xxx",picture:"static/xiangjianxiaopai.jpg",price:88.88,tips:["ttt","ttt"],detail:"xxx"},
					{name:"xxx",picture:"static/xiangjianxiaopai.jpg",price:88.88,tips:["ttt","ttt"],detail:"xxx"},
					{name:"xxx",picture:"static/xiangjianxiaopai.jpg",price:88.88,tips:["ttt","ttt"],detail:"xxx"},
					{name:"xxx",picture:"static/xiangjianxiaopai.jpg",price:88.88,tips:["ttt","ttt"],detail:"xxx"},
					{name:"xxx",picture:"static/xiangjianxiaopai.jpg",price:88.88,tips:["ttt","ttt"],detail:"xxx"},
					{name:"xxx",picture:"static/xiangjianxiaopai.jpg",price:88.88,tips:["ttt","ttt"],detail:"xxx"},
					{name:"xxx",picture:"static/xiangjianxiaopai.jpg",price:88.88,tips:["ttt","ttt"],detail:"xxx"},
					{name:"xxx",picture:"static/xiangjianxiaopai.jpg",price:88.88,tips:["ttt","ttt"],detail:"xxx"},
					{name:"xxx",picture:"static/xiangjianxiaopai.jpg",price:88.88,tips:["ttt","ttt"],detail:"xxx"},
					{name:"xxx",picture:"static/xiangjianxiaopai.jpg",price:88.88,tips:["ttt","ttt"],detail:"xxx"},
					{name:"xxx",picture:"static/xiangjianxiaopai.jpg",price:88.88,tips:["ttt","ttt"],detail:"xxx"},
					{name:"xxx",picture:"static/xiangjianxiaopai.jpg",price:88.88,tips:["ttt","ttt"],detail:"xxx"},
					{name:"xxx",picture:"static/xiangjianxiaopai.jpg",price:88.88,tips:["ttt","ttt"],detail:"xxx"},
					{name:"xxx",picture:"static/xiangjianxiaopai.jpg",price:88.88,tips:["ttt","ttt"],detail:"xxx"},
					{name:"xxx",picture:"static/xiangjianxiaopai.jpg",price:88.88,tips:["ttt","ttt"],detail:"xxx"},
					{name:"xxx",picture:"static/xiangjianxiaopai.jpg",price:88.88,tips:["ttt","ttt"],detail:"xxx"},
					{name:"xxx",picture:"static/xiangjianxiaopai.jpg",price:88.88,tips:["ttt","ttt"],detail:"xxx"},
					{name:"xxx",picture:"static/xiangjianxiaopai.jpg",price:88.88,tips:["ttt","ttt"],detail:"xxx"},
					{name:"xxx",picture:"static/xiangjianxiaopai.jpg",price:88.88,tips:["ttt","ttt"],detail:"xxx"},
					{name:"xxx",picture:"static/xiangjianxiaopai.jpg",price:88.88,tips:["ttt","ttt"],detail:"xxx"},
					{name:"xxx",picture:"static/xiangjianxiaopai.jpg",price:88.88,tips:["ttt","ttt"],detail:"xxx"},
					{name:"xxx",picture:"static/xiangjianxiaopai.jpg",price:88.88,tips:["ttt","ttt"],detail:"xxx"},
					{name:"xxx",picture:"static/xiangjianxiaopai.jpg",price:88.88,tips:["ttt","ttt"],detail:"xxx"},
					{name:"xxx",picture:"static/xiangjianxiaopai.jpg",price:88.88,tips:["ttt","ttt"],detail:"xxx"}
				],
				btnList:[{
					bgColor: "#16C2C2",
					//名称
					text: "关于",
					//字体大小
					fontSize: 28,
					//字体颜色
					color: "#fff"
				}, {
					bgColor: "#64B532",
					//名称
					text: "分享",
					//字体大小
					fontSize: 28,
					//字体颜色
					color: "#fff"
				}]
			}
		},
		components:{
		}
		,
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style>
	#styles{background-color: #202326;width: 20vw;height: 100vh;position: absolute;float: left;}
	.li{list-style: none;}
	#dishes{}
</style>

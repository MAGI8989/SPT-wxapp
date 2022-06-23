<template>
	<view class="content">
		<div id="ad" >
		</div>
		<div id="main">
			<div id="styles">
				<!-- 侧边菜品分类 -->
				<tui-list-view>
					<div v-for="item in styles" :key="item.id" style="color: #fafafa;background-color: #202326;text-align: center;margin-top: 100rpx;">
						{{item.text}}
					</div>
				</tui-list-view>
			</div>
			<div class="dishes" style="float: right;">
				<!-- 主体菜单 -->
				<!-- <tui-overflow-hidden></tui-overflow-hidden> -->
				<view>
					<u-notice-bar :text="notice" class="notice_bar" style="width: 100rpx;"></u-notice-bar>
				</view>
			</div>
		</div>
		<div id="bottom">
			<div id="bill">
				<tui-drawer :mode="bottom" :visible=false @close="closeDrawer">
					<view class="d-content">
						<tui-button height="80rpx" type="warning" shape="rightcircle" @click="closeDrawer" style="width: 100%; height: 51px; line-height: 51px; font-size: 17px; margin: 0px;" plain="">Click Me</tui-button>
					</view>
				</tui-drawer>
				<!-- <tui-fab :btnList="btnList" :left="200" :right=auto :maskClosable=true :bottom="0" :width="250" :radius="65" :custom=true  >
				</tui-fab> -->
			</div>
		</div>
		
	</view>
</template>

<script>
	export default {
		data() {
			return {
				notic:"系统尚处于开发维护阶段！！！",
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
	#styles{background-color: #202326;width: 30vw;height: 100vh;position: absolute;float: left;}
	.li{list-style: none;}
	#dishes{}
</style>

## Vue实现简单计数功能
1.加一 add函数

2.减一 sub 函数

3.清零 remove函数



### 相关代码


```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8" />
		<title>Vue简单计数器的实现</title>
		<script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js" type="text/javascript" charset="utf-8"></script>
		<style type="text/css">
			#container div{
				float: left;
			}
			#counter{
				width: 50px;
				height: 50px;
				background: greenyellow;
			}
			button{
				width: 50px;
				height: 50px;
				background: blue;
				}
		</style>
	</head>
	<body>
		<div id='container'>
			<div id="counter">{{ num }}</div>
			//添加按钮的事件监听和相关的函数绑定
			// @click='方法名称'
			// @click 是 v-on:的简写
			<button class="left" @click="add">加1</button>
			<button class="right" @click="sub">减1</button>
			<button class="remove" @click="remove">清空</button>
		</div>
		<script>
			var app = new Vue({
			//Vue实例挂载点：id="container"的DOM节点
				el:"#container",
				data:{
					num:0,
				},
				methods:{
				// 加1操作的函数
					add : function () {
						if (this.num>=10){
							alert("已经最大了，不能再加了")
						}else{
							this.num++;
						}
					},
					// 减1操作的函数
					sub : function () {
						if (this.num<=0) {
							alert("已经是0了，不能再减了")
						}else{
							this.num--;
						}
					},
					// 1清零操作的函数
					remove:function(){
						this.num=0;
					}
				}
			});
			
		</script>
	</body>
</html>
```


###  需求描述
1. 实现文本输入一条数据，在列表里面显示，并将文本框内容清空
2. 点击添加一条按钮，将添加的数据在列表页显示
3. 点击删除一条按钮，将最后一条数据删除
4. 点击移除所有按钮，将列表页内容全部清空
5. 点击删除，就将最后一条数据删除，
6. 点击隐藏按钮，将整个内容隐藏
7. 点击显示按钮，将隐藏的内容显示出来
### 代码实现

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title>Vue动态添加内容,并在列表页显示</title>
		<script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>
	</head>
	<body>
		<div id="app" v-if="show" >
		// 将输入框的内容绑定到message
			<input type="text" v-model="message"/>
			<button @click="add">添加一条</button>
			<button @click="del">删除一条</button>
			<button @click="remove">移除所有</button>
			<ul>
				<li v-for="li in lis">{{li}}</li>
			</ul>
			<button @click="hidden">隐藏</button>
		</div>
		<div id="show">
			<button @click="display">显示</button>
		</div>
		<script>
			var vm = new Vue({
				el:'#app',
				data:{
					show:true,
					message:'',
					lis:[],
				},
				methods:{
				// 添加一条数据
					add:function(){
						this.lis.push(this.message);
						this.message='';
					},
					// 删除一条数据
					del:function(){
						this.lis.pop();
					},
					// 移除所有数据
					remove:function(){
						this.lis=[];
					},
					// 将内容隐藏
					hidden:function(){
						this.show=false;
					}
				}
			});
			var vl = new Vue({
				el:'#show',
				data:{
					show:false,
				},
				methods:{
				// 将隐藏的内容显示出来
					display:function(){
						vm.show=true;
					},
				}
			});
		</script>
	</body>
</html>

```

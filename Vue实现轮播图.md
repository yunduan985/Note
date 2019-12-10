# Vue实现轮播图
### 功能描述
1.点击左尖括号图片，切换为上一张图片
2.点击右尖括号图片，切换为上一张图片
3.当前为第一张图片时，左边尖括号图片不显示
4.当前图片为最后一张图片时，右边尖括号图片不显示
### 实现原理
1.用一个数组存储图片的相对路径，通过改变数组的索引来改变图片的src属性，进而实现图片切换。
2.当前显示为第一张图片时，索引值为0(由于数组的下标是从0开始)。
3.左右边尖括号图片的显示，通过v-show属性的布尔值来控制，当数组的索引值大于0时，左边尖括号图片显示出来。
4.当数组的索引值小于数组的长度-1时，右边边尖括号图片显示出来。
### 文件结构
图片：![在这里插入图片描述](https://img-blog.csdnimg.cn/20191209160333814.png)
### 相关代码

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title>轮播图</title>
		<link rel="stylesheet" href="css/index.css" />
		<!-- <style>
			h2{
				color: #FF0000;
			}
			#center{
				width: 1000px;
				height: 750px;
				position: absolute;
				display: inline;
				left:500px ;
				top: 250px;
				display: inline;
			}
			.center .pre{
				position: relative;
				left: -328px;
				top: 287px;
			}
			.center .next{
				position: relative;
				left:327px;
				top: -284px;
			}
		</style> -->
	</head>
	<body>
		<div id="center" align="center">
			<div class="center">
				<h2>深圳中泰龙股权投资基金管理有限公司</h2>
				<a href="javascript:void(0)" @click="pre" v-show="index>0" class="pre" ><img src="images/prev.png"/></a>
				<div class="img"><img :src="imglist[index]"/></div>
				<a href="javascript:void(0)" @click="next" class="next" v-show="index<imglist.length-1"><img src="images/next.png"></a>
			</div>
		</div>
		<script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>
		<script>
			var app = new Vue({
				el:'#center',
				data:{
					index:0,
					imglist:['images/00.jpg',
							 'images/01.jpg',
							 'images/02.jpg',
							 'images/03.jpg',
							 'images/04.jpg',
							 'images/05.jpg',
							 'images/06.jpg',
							 'images/07.jpg',
							 'images/08.jpg',
							 'images/09.jpg',
							 'images/10.jpg']
				},
				methods:{
					pre:function(){
						this.index--;
					},
					next:function(){
						this.index++;
					},	
				}
			});
			// setTimeout(function(){
			// 	app.index++;
			// },2000);
			
		</script>
	</body>
</html>

```


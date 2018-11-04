<template>
	<div class="detail-page">
		<div class="video">
			<iframe src="https://player.vimeo.com/video/247494684?color=4fc08d&title=0&byline=0&portrait=0" width="95%" height="95%" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>
			<router-link to="/">
				<div class="video-back"><</div>
			</router-link>
		</div>
		<ul class="nav">
			<li v-for="item in arr">{{item}}</li>
		</ul>


		<div class="title">
			<h1>{{title}}</h1>
			<p>{{des}}</p>
		</div>


		<ul class="question">
			<li v-for="(item, index) in arrQuestion">
				<h1>{{arrTitle[index]}}</h1>
				<p v-html="item"></p>
			</li>
		</ul>
		

	</div>
</template>
<script>
	export default{
		data(){
			return{
				arr: [],
				title: '',
				des: '',
				arrQuestion:[],
				arrTitle: ["Pre-requiements", "Desciption"]
			}
		},
		mounted(){
			this.arr = ["Chapter", "Detail", "Review", "Q&A", "Notes"];


			this.title = "VUE.js development";
			this.des = "Vue (pronounced /vjuː/, like view) is a progressive framework for building user interfaces. Unlike other monolithic frameworks, Vue is designed from the ground up to be incrementally adoptable. The core library is focused on the view layer only, and is easy to pick up and integrate with other libraries or existing projects. On the other hand, Vue is also perfectly capable of powering sophisticated Single-Page Applications when used in combination with modern tooling and supporting libraries.";



			this.arrQuestion = ["Already know HTML, CSS and JavaScript.", `

			(1)Template Syntax<br/> 
			(2)Computed Properties and Watchers<br/> 
			(3)Class and Style Bindings<br/>
			(4)Conditional Rendering`];
		}
	}
</script>
<style scoped>
	.video{
		position: relative;
		height:200px;
		top:10px;
	}
	.video-back{
		position: absolute;
		top: 21px;
		left: 16px;
		text-align: center;
		color: #fff;
		font-size: 18px;
		line-height: 32px;
		border-radius: 3px;
		width: 32px;
		height: 32px;
		background: rgba(0,0,0,.5);
	}

	.nav{
		position: relative;
		z-index: 1;
		display: flex;
		box-shadow: 0 2px 4px 0 rgba(0,0,0,0.10);
	}
	.nav li{
		flex: 1;
		text-align: center;
		height: 44px;
		line-height: 44px;
		background: #fff;
		font-size: 14px;
	}
	.title{
		padding: 24px 0 0 20px;
		margin-bottom: 8px;
	}
	.title h1{
		font-size: 16px;
		color: #2B333B ;
	}
	.title p{
		font-size: 14px;
		color: #71777D;
		padding : 16px 0 34px;
		width: 335px;
	}
	.question{
		padding: 20px;
		background: #fff;
		
	}
	.question li h1{
		font-size: 14px;
		color: #2B333B; 
	}
	.question li p{
		padding:12px 0 0 30px;
		font-size: 14px;
		color: #71777D ; 
	}
	.question li:nth-child(1){
		padding-bottom: 24px;
	}
</style>
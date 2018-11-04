<template>
	<div class="home-page">
		<v-header></v-header>
		<ul class="nav">
		<router-link to="/detail">
			<li v-for="item in itemList">
				<img :src="item.imgUrl" />
				<span>{{item.name}}</span>
			</li>
		</router-link>
		</ul>
		<v-course :courseList= "array"></v-course><!-- dont forget ":" -->
		<v-footer></v-footer>
	</div>
</template>
<script>
	import Header from "@/components/header/"
	import webImg from "@/assets/web.png"
	import webserviceImg from "@/assets/webservice.png"
	import dataImg from "@/assets/data.png"
	import bigdataImg from "@/assets/bigdata.png"
	import course from "@/components/course"
	import course1 from "@/assets/course1.jpg";
	import course2 from "@/assets/course2.jpg";
	import course3 from "@/assets/course3.jpg";
	import course4 from "@/assets/course4.jpg";
	import course5 from "@/assets/course5.jpg";
	import Footer from "@/components/footer/"

	export default{
		data(){
			return{
				itemList:[]
			}
		},
		mounted(){
			this.itemList = [{
				imgUrl : webImg,
				name: 'Frontend'
			},{
				imgUrl : webserviceImg,
				name: 'Backend'
			},{
				imgUrl : dataImg,
				name: 'Database'
			},{
				imgUrl : bigdataImg,
				name: 'Cloud'
			}];

			this.array = [
				{
					imgUrl: course1,
					title: 'Java',
					msg: 'Beginning course'
				},
				{
					imgUrl: course2,
					title: 'Sed+Awk',
					msg: 'Advanced course'
				},
				{
					imgUrl: course3,
					title: 'Javescript',
					msg: 'Beginning course'
				},
				{
					imgUrl: course4,
					title: 'VUE.js',
					msg: 'Advanced course'
				},
				{
					imgUrl: course5,
					title: 'HTML5+CSS3',
					msg: 'Beginning course'
				}
			];
		},
		components:{
			'v-header':Header,
			'v-course':course,
			'v-footer':Footer
		}
	}
</script>
<style scoped>
	.nav{
		height: 100px;
		padding-top: 44px;
		background: #F3F5F7;
		overflow-x: scroll;
		white-space: nowrap;
		font-size: 0;
	}
	.nav li{
		width: 88px;
		display: inline-block;
		text-align: center;
		font-size: 14px;
	}
	.nav li img{
		display: block;
		width: 32px;
		margin: 20px auto 12px;
	}
</style>
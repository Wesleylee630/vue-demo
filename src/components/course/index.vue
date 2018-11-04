<template>
	<ul class="c-unit">
		<li v-for="item in courseList">
			<img :src="item.imgUrl" />
			<h1>{{item.title}}</h1>
			<p>{{item.msg}}</p>
		</li>
	</ul>
</template>
<script>
	export default{
		props:{
			courseList: Array
		}
	}
</script>

<style scoped>
	.c-unit{
		padding: 24px 0;
		background: #fff;
		
	}
	.c-unit li{
		position: relative;
		width: 335px;
		height: 72px;
		margin : 0 auto 24px;
		
	}
	.c-unit li img{
		position: absolute;
		width: 108px;
		border-radius: 5px;
	}
	.c-unit li h1{
		font-size: 15px;
		padding-left: 124px;
		color: #2B333B;
	}
	.c-unit li p{
		font-size: 12px;
		padding: 8px 0 0 124px;
		color: #71777D;
	}
</style>
<template>
	<div class="c-header">
		<li>Home</li>
		<li>Course</li>
		<li>Project</li>
		<li>Career</li>
		<li class="header-search"><img src="../../assets/search.png"></li>
		<li class="header-history"><img src="../../assets/history.png"></li>
	</div>
</template>
<style scoped>
.c-header{
	position:fixed;
	z-index:3;
	width:375px;
	height:50px;
	top:0px;
	background-color: #fff;
	box-shadow: 0 2px 4px 0 rgba(0,0,0,0.10);
}
.c-header li{
	float:left;
	padding-left:15px;
	line-height:50px;
	font-size:16px;
	line-height:50px;
}
.c-header img{
	height:18px;
	width:18px;
}
.c-header .header-search{
	padding-left:60px;
}
.c-header .header-search,.c-header .header-history{
	line-height:55px;
}
</style>
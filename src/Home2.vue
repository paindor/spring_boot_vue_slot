<template>
<div id="app">
	<layout>
		<template #header="header">
			<h1>{{header.title}}</h1>
		</template>
		<template #sidebar="sidebar">
			<ul class="menu">
				<li v-for="sidebar of sidebars" :key="sidebar.menu">
					<a :href="sidebar.link">{{sidebar.menu}}</a>
				</li>
			</ul>
		</template>
		<template #content="content">
			<h2>{{content.cont}}</h2>
		</template>
		<template #footer="footer">
			<h3>{{footer.foot}}</h3>
		</template>
	</layout>
</div>
</template>
<script>
import Layout from "@/components/Layout.vue"
export default{
	components : {Layout},
	data(){
		return{
			sidebars : [
				{menu : "Home", link: "#"},
				{menu : "About", link: "#"},
				{menu : "Contact", link: "#"},
				{menu : "Subject", link: "#"}
			]
		}
	}
}
</script>
<style scoped>
ul.menu {
    position:relative;
    padding: 5px 5px 5px 5px;
    list-style: none;
    font-style: italic;
}
ul.menu a {
    text-decoration:none;
}
</style>
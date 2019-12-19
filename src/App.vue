<template>
<div id="app">
	<child-form :headerText="header" :footerText="footer">
		<p>{{message}}</p>
	</child-form>
</div>
</template>
<script>
import ChildForm from "@/components/Child.vue"
export default {
	name : "app",
	components : {ChildForm},
	data(){
		return{
			header : "슬롯 헤드 테스트",
			footer : "슬롯 푸터 테스트",
			message : "APP 의 컨텐츠"
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
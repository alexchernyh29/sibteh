<template>
	<a :href="href" :class="cssClass"><slot>{{ text }}</slot></a>
</template>
<script setup>

const props = defineProps({
    text: {
        default: "Button",
        type: String
    },
    href: {
        default: "/",
        type: String
    },
    cssClass: {
        default: "buttons",
    }
})

    
</script>
<style scoped>
a.buttons {
    max-width: 160px;
	text-decoration: none;
	padding: 16px 32px;
	color: #fff;
	background-color: #3EA748;
	text-align: center;
	line-height: 20px;
	display: block;
	font: normal 16px arial;
	border-radius: 10px;
	font-family: 'CeraPro-Medium';
	font-weight: 500;
	font-size: 16px;
}
a.buttons:hover {
	background-color: #33793A;
}
a.white-border {
	border-radius: 10px;
	border: 1px solid #3EA748;
	max-width: 160px;
	text-decoration: none;
	padding: 16px 32px;
	color: #3EA748;
	background-color: #fff;
	text-align: center;
	line-height: 20px;
	display: block;
	font: normal 16px arial;
	border-radius: 10px;
	translate: 0.5s;
	font-family: 'CeraPro-Medium';
	font-weight: 500;
	font-size: 16px;
}
a.white-border:hover {
	color: #fff;
	background-color: #3EA748;
	translate: 0.5s;
}
a.white {
	max-width: 160px;
	text-decoration: none;
	padding: 16px 32px;
	color: #3EA748;
	background-color: #fff;
	text-align: center;
	line-height: 20px;
	display: block;
	font: normal 16px arial;
	border-radius: 10px;
	translate: 0.5s;
	font-family: 'CeraPro-Medium';
	font-weight: 500;
	font-size: 16px;
}
a.white:hover {
	color: #fff;
	background-color: #3EA748;
	translate: 0.5s;
}
a.buttons:not(.active):hover,
a.buttons:not(.active):focus {
	color: #fff;
}
a.buttons:not(:hover) {
	transition: 0.6s;
}
.disabled {
	transition: color 900ms linear, text-shadow 500ms linear, background-image 900ms linear;
	padding: 10px;
	color: #fff;
	background-image: linear-gradient(#828897, #5F697C);
	border-radius: 20px;
	text-shadow: 0 0 21px rgba(223, 206, 228, 0.5), 0 0 10px rgba(223, 206, 228, 0.4), 0 0 2px #2a153c;
	pointer-events: none;
	margin: 20px auto;
}
</style>
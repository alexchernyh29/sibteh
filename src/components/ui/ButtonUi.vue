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
    max-width: 200px;
	text-decoration: none;
	padding: 10px;
	color: #fff;
	background-color: #3EA748;
	text-align: center;
	line-height: 20px;
	display: block;
	margin: 20px auto;
	font: normal 17px arial;
	border-radius: 20px;
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
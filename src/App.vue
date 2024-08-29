<script setup lang="ts" vapor>
	import { ref, watch } from "vue";
	import MyAwesomeButton from "./components/MyAwesomeButton.vue";
	const amIVue = ref(true);
	const vueTitle = ref("Vite Vue!");
	watch(vueTitle, (vueTitle: string, prevVueTitle: string) => {
		document.title = vueTitle; // No bueno
	});
	function aOk(event: Event): void {
		amIVue.value = !amIVue.value;
		vueTitle.value = amIVue.value ? "Vite Vue!" : "Vite nie-Vue!";
	}
</script>

<template>
	<header>
		<button>hello i am a button</button>
	</header>
	<main>
		{{ vueTitle }}
		<MyAwesomeButton @click="aOk">
			<!-- Ten przycisk uważa przeciwnie -->
			{{ amIVue ? "Nie jestem Vue" : "Jednak jestem Vue" }}
		</MyAwesomeButton>
	</main>
</template>

<style scoped lang="scss">
	main {
		background-color: #ff0;
		button:after {
			content: "!!!";
		}
	}
</style>

<script setup lang="ts">
	import { ref, watch } from "vue";
	import Headerro from "./components/Headerro.vue";
	import Selectorro from "./components/Selectorro.vue";
	const test = ref("test");
	const keywords = [
		"C", "C++", "CMake", "JSON", "Node.js", "YAML", "Swagger", "Wikipedia",
		"Java", "PHP", "Python", "Windows", "Mac OS X", "Linux", "BSD", "Unix",
		
	];
</script>

<template>
	<div class="
		bg-zinc-100
		grid grid-cols-1
		min-h-lvh
		justify-items-center
		items-center
	">
		<div class="w-11/12 lg:w-1/2">
			<Headerro/>
			<main>
				<p class="py-2 pl-1">
					Skills:
				</p>
				<Selectorro  :options="keywords"/>
			</main>
			<footer class="text-center text-zinc-500 py-10">
				&copy; 2024 czbd. For due historical record: at this date,
				this was the easiest application question.
			</footer>
		</div>
	</div>
</template>

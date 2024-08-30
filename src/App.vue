<script setup lang="ts">
	import { ref, watch } from "vue";
	import Selectorro from "./components/Selectorro.vue";
	const test = ref("test");
	const keywords = [
		"C", "C++", "CMake", "JSON", "Node.js", "YAML", "Swagger", "Wikipedia",
		"Java", "PHP", "Python", "Windows", "Mac OS X", "Linux", "BSD", "Unix",
		
	];
</script>

<template>
	<header>
		
	</header>
	<main>
		{{  test }}
		<Selectorro :options="keywords"/>
	</main>
	<footer>
		
	</footer>
</template>
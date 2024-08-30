<template>
	<div>
		<Multiselect
			v-model="value"
			:options="options"
			:multiple="true"
			:taggable="true"
			@tag="addTag"
		></Multiselect>
	</div>
</template>

<script lang="ts">
	// So this is that Options API... Uglier tbh
	import Multiselect from "vue-multiselect";
	import "vue-multiselect/dist/vue-multiselect.css";

	export default {
		components: { Multiselect },
		props: {
			options: {
				type: Object,
				required: true
			}
		},
		data(): void {
			return {
				value: [] as string[]
			};
		},
		methods: {
			addTag(tag: string): void {
				this.options.push(tag);
				this.value.push(tag);
			}
		},
	};
</script>

<!-- This doesn't work right :( <script setup lang="ts">
	import Multiselect from "vue-multiselect";
	import "vue-multiselect/dist/vue-multiselect.css";
	
	const value: string[] = []; //the culprit
	const options: string[] = [];
	
	function addTag(tag: string): void {
		options.push(tag);
		value.push(tag);
	}
</script> -->
<script lang="ts">
	import type { Snippet } from "svelte";

	type Props = {
		children?: Snippet;
		class?: string;
	};

	const { children, ...props }: Props = $props();
</script>

<div class={"card default-colours default-margin hover " + props.class}>
	{@render children?.()}
</div>

<style lang="postcss">
	@reference "$routes/layout.css";

	.card {
	}
</style>

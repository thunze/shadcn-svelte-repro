<script lang="ts">
	import '../app.css';
	
	let { children } = $props();
</script>

<div class="flex min-h-screen w-full justify-center items-center">
	{@render children()}
</div>

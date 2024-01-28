<!-- FILE: +layout.svelte -->

<script lang="ts">
	import '../app.css';
</script>

<div style="2px solid green">
	<div class="py-10">
		<main>
			<div class="mx-auto max-w-7xl sm:px-6 lg:px-8">
				<!-- Your content -->
				<slot />
			</div>
		</main>
	</div>
</div>

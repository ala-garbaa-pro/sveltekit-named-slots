# Slots in SvelteKit - Ala GARBAA

Welcome to the "Slots in SvelteKit" repository! This project showcases the usage of slots in a SvelteKit application and is developed by Ala GARBAA.

## Overview

This repository demonstrates how to structure layouts using slots in SvelteKit, allowing for flexible and reusable components. The main focus is on the `MainLayout.svelte` component, which acts as a base layout for different pages.

## Developer Information

- **Developer:** Ala GARBAA
- **Website:** [www.alagarbaa.com](https://www.alagarbaa.com)

## Project Structure

### 1. MainLayout.svelte

This file defines the main layout structure with navigation, header, and content areas. It utilizes slots to insert dynamic content.

```svelte
<!-- FILE: ui/MainLayout.svelte -->

<!-- ... (Navigation section) ... -->

<header>
	<div class="px-4 mx-auto max-w-7xl sm:px-6 lg:px-8">
		<slot name="title">
			<h1 class="text-3xl font-bold leading-tight tracking-tight text-gray-900">
				Default Title
			</h1>
		</slot>
	</div>
</header>

<main>
	<div class="mx-auto max-w-7xl sm:px-6 lg:px-8">
		<slot />
	</div>
</main>
```

### 2. +layout.svelte

This file extends the main layout and provides additional styling.

```svelte
<!-- FILE: +layout.svelte -->

<script lang="ts">
	import '../app.css';
</script>

<div style="2px solid green">
	<div class="py-10">
		<main>
			<div class="mx-auto max-w-7xl sm:px-6 lg:px-8">
				<slot />
			</div>
		</main>
	</div>
</div>
```

### 3. +page.svelte

An example of a page using the `MainLayout` with a custom title.

```svelte
<!-- FILE: +page.svelte -->

<script lang="ts">
	import MainLayout from './ui/MainLayout.svelte';
</script>

<MainLayout>
	<h1 slot="title" class="text-4xl font-bold leading-tight tracking-tight text-blue-900">
		Dashboard
	</h1>

	This is home page content example!
</MainLayout>
```

### 4. profile/+page.svelte

Another example page showcasing a personalized profile layout.

```svelte
<!-- FILE: profile/+page.svelte -->

<script lang="ts">
	import MainLayout from '../ui/MainLayout.svelte';
</script>

<MainLayout>
	<h1 slot="title" class="text-4xl font-bold leading-tight tracking-tight text-blue-900">
		Hello, <b>Ala! 🙋</b>
	</h1>

	O My profile! My name is ....
</MainLayout>
```

Feel free to explore and modify the code to fit your specific needs. If you have any questions or feedback, don't hesitate to reach out to Ala GARBAA through [www.alagarbaa.com](https://www.alagarbaa.com). Happy coding!
<!-- FILE: ui/MainLayout.svelte -->

<div class="py-10">
	<nav class="bg-gray-800">
		<div class="mx-auto max-w-7xl px-2 sm:px-6 lg:px-8">
			<div class="relative flex h-16 items-center justify-between">
				<div class="flex flex-1 items-center justify-center sm:items-stretch sm:justify-start">
					<div class="hidden sm:ml-6 sm:block">
						<div class="flex space-x-4">
							<!-- Current: "bg-gray-900 text-white", Default: "text-gray-300 hover:bg-gray-700 hover:text-white" -->
							<a
								href="/"
								class="bg-gray-900 text-white rounded-md px-3 py-2 text-sm font-medium"
								aria-current="page">Dashboard</a
							>
							<a
								href="/profile"
								class="text-gray-300 hover:bg-gray-700 hover:text-white rounded-md px-3 py-2 text-sm font-medium"
								>Profile</a
							>
						</div>
					</div>
				</div>
			</div>
		</div>

		<!-- Mobile menu, show/hide based on menu state. -->
		<div class="sm:hidden" id="mobile-menu">
			<div class="space-y-1 px-2 pb-3 pt-2">
				<!-- Current: "bg-gray-900 text-white", Default: "text-gray-300 hover:bg-gray-700 hover:text-white" -->
				<a
					href="/"
					class="bg-gray-900 text-white block rounded-md px-3 py-2 text-base font-medium"
					aria-current="page">Dashboard</a
				>
				<a
					href="/profile"
					class="text-gray-300 hover:bg-gray-700 hover:text-white block rounded-md px-3 py-2 text-base font-medium"
					>profile</a
				>
			</div>
		</div>
	</nav>

	<header>
		<div class="px-4 mx-auto max-w-7xl sm:px-6 lg:px-8">
			<slot name="title"
				><h1 class="text-3xl font-bold leading-tight tracking-tight text-gray-900">
					Dashboard
				</h1></slot
			>
		</div>
	</header>
	<main>
		<div class="mx-auto max-w-7xl sm:px-6 lg:px-8">
			<!-- Your content -->
			<slot />
		</div>
	</main>
</div>

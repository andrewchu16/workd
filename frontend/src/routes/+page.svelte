<svelte:head>
	<title>Work'd</title>
</svelte:head>
<main class="h-screen w-screen">
    <div class="h-full w-full bg-primary/90 flex flex-col items-center justify-center">
        <div class="h-2/3 w-full flex flex-col items-center justify-center">
            <h1 class="font-display text-5xl text-white display-spacing suffix-animation">work</h1>
            <h2 class="pt-4 text-white">Take back your day.</h2>
        </div>
        <a
            class="py-3 px-6 bg-white rounded-full text-primary hover:bg-neutral-200 text-xl"
            href="/onboarding">Get Started</a
        >
    </div>
</main>

<style>
	main {
		background-image: url('/onboarding-bg.jpg');
		background-size: cover;
		background-position: center;
	}

	.suffix-animation::after {
		animation: delete-suffix 4s alternate-reverse infinite;
		content: 'day';
		text-decoration-skip-ink: none;
		@apply text-white;
	}

	@keyframes delete-suffix {
		0% {
			content: 'day?';
			@apply text-white;
		}

		40% {
			content: 'day?';
			@apply text-white;
		}

		45% {
			content: 'day';
		}

		50% {
			content: 'da';
		}

		55% {
			content: 'd';
		}

		100% {
			content: "'d";
			@apply text-secondary;
		}
	}
</style>

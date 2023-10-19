<script>
	import Counter from './Counter.svelte';
	import welcome from '$lib/images/clever-logo.webp';
	import welcome_fallback from '$lib/images/clever-logo.png';
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
	<h1>
		<span class="welcome">
			<picture>
				<source srcset={welcome} type="image/webp" />
				<a href="https://clever-cloud.com">
				<img src={welcome_fallback} alt="Clever Cloud logo" />
				</a>
			</picture>
		</span>

		Welcome to this <br />SvelteKit kawaï app
	</h1>

	<h2>
		a demo app for <strong>Clever Cloud</strong>
	</h2>

	<Counter />
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
		position: relative;
	}
	section::before {
	  content: "";
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(255, 255, 255, 0.9);
      z-index: -1;
    }

	h1 {
		width: 100%;
	}

	.welcome {
		display: block;
		width: 100%;
		height: 100%;
		padding: 0 0 calc(100% * 495 / 2048) 0;
		
	}

	.welcome img {
		position: absolute;
		width: 100%;
		height: auto;
		top: 0;
		display: block;
		
	}
</style>

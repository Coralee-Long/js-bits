<script>
	import Prism from 'svelte-prism';
</script>

<svelte:head>
	<title>Objects</title>
	<meta name="objects" content="Javascript Objects" />
</svelte:head>

<div class="text-column">
	<h1>Objects</h1>

	<Prism language="javascript">
		{`test('Check title', async () => {
	const title = await firstWindow.title();
	expect(title).toBe('MEMENTO - Svelte, TailwindCSS, Electron and TypeScript');
});`}
	</Prism>

	<pre>npm create svelte@latest</pre>

	<p>
		The page you're looking at is purely static HTML, with no client-side interactivity needed.
		Because of that, we don't need to load any JavaScript. Try viewing the page's source, or opening
		the devtools network panel and reloading.
	</p>

	<p>
		The <a href="/sverdle">Sverdle</a> page illustrates SvelteKit's data loading and form handling. Try
		using it with JavaScript disabled!
	</p>
</div>

<style>
</style>

<script>
	import Prism from 'svelte-prism';
</script>

<svelte:head>
	<title>Javascript Loops</title>
	<meta name="loops" content="Javascript Loops" />
</svelte:head>

<div class="text-column">
	<h1>Javascript Loops</h1>
	<h2>For Loops</h2>
	<p>
		Basic example of a <a
			href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Loops_and_iteration#for_statement"
		>
			For Loop</a
		>
	</p>
	<Prism language="javascript">
		{`for (let i = 1, i <= 5; i++) {
		console.log('loop number', i);
	}

	// loop number 1
	// loop number 2
	// loop number 3
	// loop number 4
	// loop number 5


for (let i = 1, i <= 10; i += 3) {
		console.log('Total:', i);
	}
console.log('Loop finished')

	// Total: 1
	// Total: 4
	// Total: 7
	// Total: 10
	// Loop finished

`}
	</Prism>
	<h2>Infinite Loops</h2>
	<Prism language="javascript">
		{`This would create an Infinite Loop:
			
	for (let i = 1, i > 0; i++) {
		console.log(i);
	}

`}
	</Prism>
</div>

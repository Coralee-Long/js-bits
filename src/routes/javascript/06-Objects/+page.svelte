<script>
	import Prism from 'svelte-prism';
</script>

<svelte:head>
	<title>Javascript Objects</title>
	<meta name="objects" content="Javascript Objects" />
</svelte:head>

<div class="text-column">
	<h1>Javascript Objects</h1>
	<h2>Key Points</h2>

	<p>Objects are collections of properties</p>
	<p>Properties are a key-value pair</p>
	<p>Rather than accessing data using an index, we use custom keys</p>
	<p>Objects don't rely on list order (like an Array would)</p>

	<Prism language="javascript">
		{`/// JAVASCRIPT OBJECTS: 

You can use 'const' because the variable is referencing 
the object, rather than holding the value.

const fitBitData = {
	totalSteps: 308728,
	totalKms: 211.7,
	avgCalorieBurn: 5755,
	workoutsThisWeek: '5 of 7',
	avgGoodSleep: '2:44'
}

Values can be retrieved using dot-notation:

//  fitBitData.avgCalorieBurn -> 5755

//  fitBitData.workoutsThisWeek -> '5 of 7'
`}
	</Prism>

	<p>Keys are actually being converted into strings:</p>
	<Prism language="javascript">
		{`const fitBitData = {
	totalSteps: 308728, 
	45: 'forty-five' 
}

// fitBitData.totalSteps -> 308728

// fitBitData.45 -> Uncaught SyntaxError`}
	</Prism>
	<p>
		To access a key that is a number/symbol or not a valid Javascript identifier, you need to use
		the square brackets
	</p>
	<Prism language="javascript"
		>{`const numbers = {
	100: 'one hundred',
	16. 'sixteen'
	}

	// numbers.100 -> Uncaught SyntaxError

	// numbers.[100] -> 'one hundred'
`}
	</Prism>

	<p>Example of an Invalid Javascript Identifier:</p>

	<Prism language="javascript"
		>{`let 76trombones = 'song'; // 76trombones -> Invalid or unexpected token
`}
	</Prism>

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
	ul {
		line-height: 1.7rem;
	}
	pre {
		width: 90%;
	}
</style>

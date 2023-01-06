<script>
	import Prism from 'svelte-prism';

	const test = {
		100: 'here is my value'
	};

	// console.log('test100', test.100);
	console.log(test[100]);
	console.log(test['100']);
</script>

<svelte:head>
	<title>Javascript Objects</title>
	<meta name="objects" content="Javascript Objects" />
</svelte:head>

<div class="text-column">
	<h1>Javascript Objects</h1>
	<h2>Key-Value Pairs</h2>

	<p>Objects are collections of Properties, and Properties are a key-value pairs:</p>
	<Prism language="javascript">
		{`Rather than accessing data using an index (like with Arrays), we use custom keys: 

const user = {
// 🔑 key        // 💎 value     
	name:         'Rich Harris', // string
	pets:          3, // number
	petNames:      ['Alpha', 'Bravo', 'Charlie'], // array
	isMarried:     true, // boolean
}

Values can be retrieved using Dot-Notation:

//  user.name -> 'Rich Harris'
//  user.pets -> 3
//  user.isMarried -> true
`}
	</Prism>

	<p>Objects don't rely on list order (like Arrays would):</p>
	<Prism language="javascript">
		{`You can use 'const' because the variable is referencing 
the object, rather than holding the value.

const fitBitData = {
	totalSteps: 308728,
	totalKms: 211.7,
	avgCalorieBurn: 5755,
	workoutsThisWeek: '5 of 7',
	avgGoodSleep: '2:44'
};

Values can be retrieved using Dot-Notation:

//  fitBitData.avgCalorieBurn -> 5755
//  fitBitData.workoutsThisWeek -> '5 of 7'
`}
	</Prism>

	<p>Keys are actually being converted and stored and stored as strings in Javascript:</p>
	<Prism language="javascript">
		{`const fitBitData = {
	totalSteps: 308728,  
	45: 'forty-five' // Javascript sees it as: '45': 'forty-five'
}

// fitBitData.totalSteps -> 308728
// fitBitData.45 -> Uncaught SyntaxError
// fitBitData.[45] -> 'forty-five'
		`}
	</Prism>

	<p>
		To access a key that is a number/symbol or not <a
			href="	https://patelhemil.medium.com/javascript-rules-for-valid-variable-names-3ba80ae09250"
			>valid Javascript Identifier</a
		>, you need to use the square brackets
	</p>
	<Prism language="javascript">
		{`const numbers = {
	100: 'one hundred',
	16. 'sixteen'
	}

	// numbers.100 -> Uncaught SyntaxError
	// numbers[100] -> 'one hundred'
	// numbers['100'] -> 'one hundred'
`}
	</Prism>

	<p>
		Example of an <a
			href="	https://patelhemil.medium.com/javascript-rules-for-valid-variable-names-3ba80ae09250"
			>Invalid Javascript Identifier:</a
		>
	</p>

	<Prism language="javascript"
		>{`let 76trombones = 'song'; // 76trombones -> Invalid or unexpected token
`}
	</Prism>

	<p>
		Using <a href="https://eslint.org/docs/latest/rules/dot-notation">Dot-Notation</a> with square brackets
		can also be used for variables:
	</p>

	<Prism language="javascript"
		>{`const palette = {
			red: '#FF0000';
			blue: '#0000FF';
			yellow: '#FFFF00';
	}; 

	// palette.red -> '#FF0000'
	// palette[red] -> Reference Error: red is not defined
	// palette['red'] -> '#FF0000'


Using Dot Notation to access a variable:

let myFavColor = 'red';

	// palette[myFavColor] -> '#FF0000'
	// palette.myFavColor -> undefined

`}
	</Prism>

	<h2>Adding Properties to an Object</h2>

	<p>
		<a href="https://www.w3schools.com/js/js_object_properties.asp">Object Properties</a> can be
		added using <a href="https://eslint.org/docs/latest/rules/dot-notation">Dot-Notation</a> or square
		brackets:
	</p>

	<Prism language="javascript"
		>{`let userReviews = {};

userReviews.myFriendJoe100 = 1;
userReviews['myFriendJack123'] = 3;

userReviews.myFriendJoe100 ++;        // Add 1
userReviews['myFriendJack123'] += 2;  // Add 2

// userReviews -> {myFriendJoe100: 2, myFriendJack123: 5;

`}
	</Prism>

	<h2>Nested Arrays & Objects</h2>
	<!-- <p>
		The page you're looking at is purely static HTML, with no client-side interactivity needed.
		Because of that, we don't need to load any JavaScript. Try viewing the page's source, or opening
		the devtools network panel and reloading.
	</p>

	<p>
		The <a href="/sverdle">Sverdle</a> page illustrates SvelteKit's data loading and form handling. Try
		using it with JavaScript disabled!
	</p> -->
</div>

<style>
	ul {
		line-height: 1.7rem;
	}
	pre {
		width: 90%;
	}
</style>

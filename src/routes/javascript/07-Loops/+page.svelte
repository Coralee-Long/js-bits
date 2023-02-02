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
		{`
	for ( let i = 1, i <= 5; i++ ) {
		console.log('loop number', i);
	}

	// loop number 1
	// loop number 2
	// loop number 3
	// loop number 4
	// loop number 5


	for ( let i = 1, i <= 10; i += 3 ) {
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
		{`
This would create an Infinite Loop:

	for ( let i = 1, i > 0; i++ ) {
		console.log(i);
	}

`}
	</Prism>

	<h2>For Loops & Arrays</h2>
	<p>To access items in an array, we can use their index numbers</p>
	<Prism language="javascript">
		{`
	const animals = ['lions', 'tigers', 'bears'];

	for ( let i = 0; i < animals.length; i++ ) {
		console.log(animals[i]);
	}

	// lions -> animals[0]
	// tigers -> animals[1]
	// bears -> animals[2]

`}
	</Prism>

	<h2>Nested For Loops</h2>
	<Prism language="javascript">
		{`
	Looping through an Array:

	const myStudents = [
		{
			firstName: 'Abby',
			grade: 97
		},
		{
			firstName: 'Benji',
			grade: 56
		},
		{
			firstName: 'Carol',
			grade: 81
		}
	];

	for (let i = 0; i < myStudents.length; i++) {
		let student = myStudents[i];
		console.log(student.firstName, student.grade);
	};

	// Abby 97
	// Benji 56
	// Carol 81


	Looping through a String (use word.length -1 because you don't 
	necessarily know the length of the word being used):

	const word = "cat";

	for ( let i = word.length -1; i >= 0, i++ ) {
		console.log(i)
	}

	// c
	// a
	// t



`}
	</Prism>
</div>

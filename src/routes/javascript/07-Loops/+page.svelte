<script>
	import Prism from 'svelte-prism';
	import SubHeader from '/src/routes/components/SubHeader.svelte';

	let text;
</script>

<svelte:head>
	<title>Javascript Loops</title>
	<meta name="loops" content="Javascript Loops" />
</svelte:head>

<div class="text-column">
	<h1>Javascript Loops</h1>
	<SubHeader text="For Loops" />
	<!-- <div class="subheaderShape">
		<h2>For Loops</h2> -->
	<!-- </div> -->
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

	<p>Looping through an Array</p>

	<Prism language="javascript">
		{`
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

	let total = 0;

	for (let i = 0; i < myStudents.length; i++) {

		let student = myStudents[i];
		console.log(student.firstName, student.grade);
			// Abby 97
			// Benji 56
			// Carol 81

		let total += student.grade;
		console.log(total / myStudents.length;)
			// 78
	};
`}
	</Prism>
	<br />
	<p>
		Looping through a String (use word.length -1 because you don't necessarily know the length of
		the word being used)
	</p>
	<Prism>
		{`
	const word = "cat";

	for ( let i = word.length -1; i >= 0, i++ ) {
		console.log(i)
	}

	// c
	// a
	// t
	`}
	</Prism>

	<h2>Nested Loops</h2>
	<p>Basic Example of Nested Loops</p>
	<Prism language="javascript">
		{`
// OUTER LOOP:
	for (let i = 100; i <= 300; i += 100) {
	console.log('OUTER LOOP', i);
// INNER LOOP:
		for (let j = 1; j <= 3; j++) {
		console.log('  INNER LOOP', j);
		}
	}

	// OUTER LOOP 100
	//   INNER LOOP 1
	//   INNER LOOP 2
	//   INNER LOOP 3
	// OUTER LOOP 200
	//   INNER LOOP 1
	//   INNER LOOP 2
	//   INNER LOOP 3
	// OUTER LOOP 300
	//   INNER LOOP 1
	//   INNER LOOP 2
	//   INNER LOOP 3
`}
	</Prism>

	<p>Nested Loops example</p>
	<Prism language="javascript">
		{`
const sudokuBoard = [
	[1, 2, 3],
	[4, 5, 6],
	[7, 8, 9]
];

// Sum of numbers on Sodoku Board:

let total = 0;

for (let i = 0; i < sudokuBoard.length; i++) {
// Loop through board to extract each row
let row = sudokuBoard[i];
console.log(row);
	// [1, 2, 3]
	// [4, 5, 6]
	// [7, 8, 9]

// Loop through each row to extract the numbers in the row
	for (let j = 0; j < row.length; j++) {
	total += row[j];
	}
}
console.log(total);
	// 45 (sum of all the numbers)
`}
	</Prism>

	<h2>While Loops</h2>
	<Prism language="javascript">
		{`
These 2 loops do essentially the same thing:

	let i = 0; // For While-Loops you have to declare the variable beforehand
	while (i <= 3) {
		console.log('while-loop', i);
		i++;
	}
		// while-loop 0
		// while-loop 1
		// while-loop 2
		// while-loop 3

	for (let j = 0; j <= 3; j++) {
		console.log('if-loop', j);
	}
		// if-loop 0
		// if-loop 1
		// if-loop 2
		// if-loop 3
`}
	</Prism>
</div>

<!-- <h2></h2>
	<p>
	</p>
	<Prism language="javascript">
		{`

`}
	</Prism> -->

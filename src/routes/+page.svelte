<script lang="ts">
	const test = 'Hey';
	const words = ['One', 'Two', 'Three'];

	let typedCharacters: string[] = [];
	let timer = 60;

	const handleTypedCharacter = (e: KeyboardEvent) => {
		typedCharacters.push(e.key);
		typedCharacters = typedCharacters;
	};

	// const timerInterval = setInterval(() => {
	// 	timer = timer - 1;
	// 	if (timer === 0) {
	// 		clearInterval(timerInterval);
	// 	}
	// }, 1000);
</script>

<h1>{test}</h1>
<p>{timer}</p>
<div on:keypress={handleTypedCharacter} tabindex="0" role="textbox">
	{#each typedCharacters as character}
		<span>{character}</span>
	{/each}
	{#each words as word}
		<p>{word}</p>
	{/each}
</div>

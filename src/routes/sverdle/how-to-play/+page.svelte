<svelte:head>
	<title>Как играть в Слова</title>
	<meta name="description" content="Как играть в Слова" />
</svelte:head>

<div class="text-column">
	<h1>Как играть в Слова?</h1>

	<p>
		Это клон <a href="https://www.nytimes.com/games/wordle/index.html">Wordle</a>, игры в угадывание слов. Для игры введите английское слово из пяти букв. Например:
	</p>

	<div class="example">
		<span class="close">r</span>
		<span class="missing">i</span>
		<span class="close">t</span>
		<span class="missing">z</span>
		<span class="exact">y</span>
	</div>

	<p>
		Буква <span class="exact">y</span> находится в нужном месте. <span class="close">r</span> и
		<span class="close">t</span>
		равильные буквы, но не в том месте. Остальные буквы неправильные и их можно отбросить. Давайте один пример:
	</p>

	<div class="example">
		<span class="exact">p</span>
		<span class="exact">a</span>
		<span class="exact">r</span>
		<span class="exact">t</span>
		<span class="exact">y</span>
	</div>

	<p>На этот раз мы угадали! У вас есть  <strong>шесть</strong> попыток, чтобы угадать слово.</p>

	<p>
		В отличие от оригинального Wordle, наша игра работает на сервере, а не в браузере, что делает невозможным мошенничество. Для отправки данных он использует <code>&lt;form&gt;</code> файлы cookie, а это значит, что вы можете играть даже с отключенным JavaScript!
	</p>
</div>

<style>
	span {
		display: inline-flex;
		justify-content: center;
		align-items: center;
		font-size: 0.8em;
		width: 2.4em;
		height: 2.4em;
		background-color: white;
		box-sizing: border-box;
		border-radius: 2px;
		border-width: 2px;
		color: rgba(0, 0, 0, 0.7);
	}

	.missing {
		background: rgba(255, 255, 255, 0.5);
		color: rgba(0, 0, 0, 0.5);
	}

	.close {
		border-style: solid;
		border-color: var(--color-theme-2);
	}

	.exact {
		background: var(--color-theme-2);
		color: white;
	}

	.example {
		display: flex;
		justify-content: flex-start;
		margin: 1rem 0;
		gap: 0.2rem;
	}

	.example span {
		font-size: 1.4rem;
	}

	p span {
		position: relative;
		border-width: 1px;
		border-radius: 1px;
		font-size: 0.4em;
		transform: scale(2) translate(0, -10%);
		margin: 0 1em;
	}
</style>

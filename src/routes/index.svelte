<script>
	/** 
	 *
	 * var quotes = <String, String>{
	    "A vida é feita de quatro dias e meio": "4dias",
	    "Analisa bem as situações. Trabalha para tudo o que pode ocorrer":
	        "primeira",
	    "Todos os que estão para lá são inimigos e querem deixar-te mal": "segunda",
	    "Tens de pensar, não observar. Assim nunca mais fazes nada por ti":
	        "terceira",
	    "Sucesso é a soma de pequenos fracassos": "quarta",
	    "Às vezes as coisas não nos parecem importantes, mas a qualquer momento podem ser":
	        "quinta",
	    "A melhor forma de ultrapassar os problemas é andando": "sexta",
	    "Os idiotas são aqueles que pensam": "setima",
	    "A vida é uma aventura, logo, qual é o stress?": "oitava",
	  };
	 */
	
	import { tick } from 'svelte';

	const quotes = [
		["A vida é feita de quatro dias e meio", "4dias"],
		["Analisa bem as situações. Trabalha para tudo o que pode ocorrer", "primeira"],
		["Todos os que estão para lá são inimigos e querem deixar-te mal", "segunda"],
		["Tens de pensar, não observar. Assim nunca mais fazes nada por ti", "terceira"],
		["Sucesso é a soma de pequenos fracassos", "quarta"],
		["Às vezes as coisas não nos parecem importantes, mas a qualquer momento podem ser", "quinta"],
		["A melhor forma de ultrapassar os problemas é andando", "sexta"],
		["Os idiotas são aqueles que pensam", "setima"],
		["A vida é uma aventura, logo, qual é o stress?", "oitava"]
	];

	let randomNumber = 0;

	const intervalId = setInterval(() => {
	  randomNumber = Math.floor(Math.random() * quotes.length);
	}, 7000);	
</script>

<div class="w-screen h-screen flex flex-col space-y-10 text-center items-center justify-center px-5" style="background-image: url('/{quotes[randomNumber][1]}.png'); background-position: center; background-repeat: no-repeat;">
	<h1 class="text-2xl font-bold text-white">Já dizia o Jorge...</h1>
	<p class="text-3xl font-bold text-white italic">"{quotes[randomNumber][0]}"</p>
</div>
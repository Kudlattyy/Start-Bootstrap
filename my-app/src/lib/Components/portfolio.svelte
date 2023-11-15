<script lang="ts">
	import { fly } from 'svelte/transition';

	import Cabin from '$lib/Images/cabin.png';
	import Cake from '$lib/Images/cake.png';
	import Circus from '$lib/Images/circus.png';
	import Game from '$lib/Images/game.png';
	import Safe from '$lib/Images/safe.png';
	import Submarine from '$lib/Images/submarine.png';
	import PlaceHolder from '$lib/Images/placeholder.jpg';

	let boolean = false;

	function OpenMenu() {
		boolean = true;
	}

	function OffMenu() {
		boolean = false;
	}

	type oferta = {
		Tittle: string;
		src: string;
	};

	let oferty: oferta[] = [
		{
			Tittle: 'Log Cabin',
			src: Cabin
		},
		{
			Tittle: 'Cake',
			src: Cake
		},
		{
			Tittle: 'Circus',
			src: Circus
		},
		{
			Tittle: 'Game',
			src: Game
		},
		{
			Tittle: 'Safe',
			src: Safe
		},
		{
			Tittle: 'Submarine',
			src: Submarine
		}
	];
</script>

<body>
	{#if boolean == true}
		<div class="main3" transition:fly={{ delay: 500, duration: 500 }}>
			<div class="Information-Menu">
				{#each oferty as oferta}
					<div class="test">
						<img src={oferta.src} alt="">
					</div>
				{/each}
				<button on:click={OffMenu}>dsasdasdasdadsda</button>
			</div>
		</div>
	{/if}

	<section class="main2">
		<div class="Containers">
			<div class="Tittle2">Portfolio</div>
			<div class="Test">
				<div class="Projects">
					<div class="item item-1"><img class="Size" src={Cabin} alt="" on:click={OpenMenu} /></div>
					<div class="item item-2"><img class="Size" src={Cake} alt="" on:click={OpenMenu} /></div>
					<div class="item item-3">
						<img class="Size" src={Circus} alt="" on:click={OpenMenu} />
					</div>
					<div class="item item-4"><img class="Size" src={Game} alt="" on:click={OpenMenu} /></div>
					<div class="item item-5"><img class="Size" src={Safe} alt="" on:click={OpenMenu} /></div>
					<div class="item item-6">
						<img class="Size" src={Submarine} alt="" on:click={OpenMenu} />
					</div>
				</div>
			</div>
		</div>

		<slot />
	</section></body
>

<style lang="scss">
	@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@600&display=swap');
	.main2 {
		height: 100vh;
		width: 100%;
		.Tittle2 {
			height: 20vh;
			width: 100%;
			display: flex;
			justify-content: center;
			align-items: center;
			font-family: 'Montserrat', sans-serif;
			font-size: 64px;
			color: #2c3e50;
		}
		.Test {
			height: 80vh;
			width: 100%;
			display: grid;
			place-items: center;
			.Projects {
				display: grid;
				grid-template-columns: 500px 500px 500px;
				grid-template-rows: 350px 350px;
				grid-gap: 50px;
				.Size {
					height: 350px;
					width: 500px;
					border-radius: 25px;
					transition-duration: 2s;
				}
				.Size:hover {
					filter: blur(5px);
				}
			}
		}
	}

	.main3 {
		width: 100vw;
		height: 100vh;
		background-color: rgba(37, 37, 37, 0.8);
		position: absolute;
		z-index: 10;
		display: grid;
		place-items: center;
		.Information-Menu {
			width: 50vw;
			height: 95vh;
			display: grid;
			place-items: center;
			border-radius: 10px;
			background-color: #ffffff;
		}
	}
</style>

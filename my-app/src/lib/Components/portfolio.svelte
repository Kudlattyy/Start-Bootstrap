<script lang="ts">
	import { fly } from 'svelte/transition';

	import Cabin from '$lib/Images/cabin.png';
	import Cake from '$lib/Images/cake.png';
	import Circus from '$lib/Images/circus.png';
	import Game from '$lib/Images/game.png';
	import Safe from '$lib/Images/safe.png';
	import Submarine from '$lib/Images/submarine.png';
	import Tittle from './Tittle.svelte';

	let boolean = false;

	let selectedOffer: oferta | null = null;

	function OpenMenu(offer: oferta) {
		boolean = true;
		selectedOffer = offer;
	}

	function OffMenu() {
		boolean = false;
		selectedOffer = null;
	}

	type oferta = {
		Tittle: string;
		src: string;
		Description: string;
	};

	let oferty: oferta[] = [
		{
			Tittle: 'Log Cabin',
			src: Cabin,
			Description:
				'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Mollitia neque assumenda ipsam nihil, molestias magnam, recusandae quos quis inventore quisquam velit asperiores, vitae? Reprehenderit soluta, eos quod consequuntur itaque. Nam.'
		},
		{
			Tittle: 'Tasty Cake',
			src: Cake,
			Description:
				'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Mollitia neque assumenda ipsam nihil, molestias magnam, recusandae quos quis inventore quisquam velit asperiores, vitae? Reprehenderit soluta, eos quod consequuntur itaque. Nam.'
		},
		{
			Tittle: 'Circus Tent',
			src: Circus,
			Description:
				'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Mollitia neque assumenda ipsam nihil, molestias magnam, recusandae quos quis inventore quisquam velit asperiores, vitae? Reprehenderit soluta, eos quod consequuntur itaque. Nam.'
		},
		{
			Tittle: 'Controller',
			src: Game,
			Description:
				'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Mollitia neque assumenda ipsam nihil, molestias magnam, recusandae quos quis inventore quisquam velit asperiores, vitae? Reprehenderit soluta, eos quod consequuntur itaque. Nam.'
		},
		{
			Tittle: 'Locked Safe',
			src: Safe,
			Description:
				'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Mollitia neque assumenda ipsam nihil, molestias magnam, recusandae quos quis inventore quisquam velit asperiores, vitae? Reprehenderit soluta, eos quod consequuntur itaque. Nam.'
		},
		{
			Tittle: 'Submarine',
			src: Submarine,
			Description:
				'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Mollitia neque assumenda ipsam nihil, molestias magnam, recusandae quos quis inventore quisquam velit asperiores, vitae? Reprehenderit soluta, eos quod consequuntur itaque. Nam.'
		}
	];
</script>

<body>
	{#if boolean == true}
		<section class="Fly-Menu">
			<div class="Container" transition:fly={{ delay: 500, duration: 500 }}>
				<div class="Information-Menu">
					{#if selectedOffer}
						<div class="Title">
							<h2>{selectedOffer.Tittle}</h2>
							<div class="Idk">
								<div class="divider-custom">
									<div class="divider-custom-line" />
									<div class="divider-custom-icon">
										<svg
											class="svg-inline--fa fa-star"
											aria-hidden="true"
											focusable="false"
											data-prefix="fas"
											data-icon="star"
											role="img"
											xmlns="http://www.w3.org/2000/svg"
											viewBox="0 0 576 512"
											data-fa-i2svg=""
											><path
												fill="currentColor"
												d="M316.9 18C311.6 7 300.4 0 288.1 0s-23.4 7-28.8 18L195 150.3 51.4 171.5c-12 1.8-22 10.2-25.7 21.7s-.7 24.2 7.9 32.7L137.8 329 113.2 474.7c-2 12 3 24.2 12.9 31.3s23 8 33.8 2.3l128.3-68.5 128.3 68.5c10.8 5.7 23.9 4.9 33.8-2.3s14.9-19.3 12.9-31.3L438.5 329 542.7 225.9c8.6-8.5 11.7-21.2 7.9-32.7s-13.7-19.9-25.7-21.7L381.2 150.3 316.9 18z"
											/></svg
										>
									</div>
									<div class="divider-custom-line" />
								</div>
							</div>
						</div>
						<div class="Photo"><img class="sizePhoto" src={selectedOffer.src} alt="" /></div>
						<div class="Description"><p>{selectedOffer.Description}</p></div>
					{/if}
					<button on:click={OffMenu}>
						<svg
							class="svg-x"
							aria-hidden="true"
							focusable="false"
							data-prefix="fas"
							data-icon="xmark"
							role="img"
							xmlns="http://www.w3.org/2000/svg"
							viewBox="0 0 320 512"
							data-fa-i2svg=""
							><path
								fill="currentColor"
								d="M310.6 150.6c12.5-12.5 12.5-32.8 0-45.3s-32.8-12.5-45.3 0L160 210.7 54.6 105.4c-12.5-12.5-32.8-12.5-45.3 0s-12.5 32.8 0 45.3L114.7 256 9.4 361.4c-12.5 12.5-12.5 32.8 0 45.3s32.8 12.5 45.3 0L160 301.3 265.4 406.6c12.5 12.5 32.8 12.5 45.3 0s12.5-32.8 0-45.3L205.3 256 310.6 150.6z"
							/></svg
						>
						Close Window</button
					>
				</div>
			</div>
		</section>
	{/if}

	<section class="Portfolio">
		<div class="Containers">
			<div class="Header">Portfolio</div>
			<div class="Idk">
				<div class="divider-custom">
					<div class="divider-custom-line" />
					<div class="divider-custom-icon">
						<svg
							class="svg-inline--fa fa-star"
							aria-hidden="true"
							focusable="false"
							data-prefix="fas"
							data-icon="star"
							role="img"
							xmlns="http://www.w3.org/2000/svg"
							viewBox="0 0 576 512"
							data-fa-i2svg=""
							><path
								fill="currentColor"
								d="M316.9 18C311.6 7 300.4 0 288.1 0s-23.4 7-28.8 18L195 150.3 51.4 171.5c-12 1.8-22 10.2-25.7 21.7s-.7 24.2 7.9 32.7L137.8 329 113.2 474.7c-2 12 3 24.2 12.9 31.3s23 8 33.8 2.3l128.3-68.5 128.3 68.5c10.8 5.7 23.9 4.9 33.8-2.3s14.9-19.3 12.9-31.3L438.5 329 542.7 225.9c8.6-8.5 11.7-21.2 7.9-32.7s-13.7-19.9-25.7-21.7L381.2 150.3 316.9 18z"
							/></svg
						>
					</div>
					<div class="divider-custom-line" />
				</div>
			</div>

			<div class="Content">
				<div class="Projects">
					{#each oferty as oferta}
						<div class="test">
							<img class="Size" src={oferta.src} alt="" />
							<div class="Size-Change" on:click={() => OpenMenu(oferta)} />
						</div>
					{/each}
				</div>
			</div>
		</div>

		<slot />
	</section>
</body>

<style lang="scss">
	@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@600&display=swap');
	.Portfolio {
		height: 100vh;
		width: 100%;
		z-index: 100;
		.Header {
			height: 5vh;
			width: 100%;
			display: grid;
			place-items: center;
			margin-top: 10vh;
			font-family: var(--base-font-bold);
			font-weight: 700;
			text-transform: uppercase;
			font-size: var(--tittle-font-size);
			color: var(--base-font-color-blue);
		}
		.Content {
			height: 70vh;
			width: 100%;
			display: grid;
			place-items: center;
			.Projects {
				display: grid;
				grid-template-columns: 400px 400px 400px;
				grid-template-rows: 288px 288px;
				grid-gap: 50px;
				.Size {
					height: 288px;
					width: 400px;
					border-radius: 25px;
					transition-duration: 1s;
				}
				.Size:hover {
					filter: blur(5px);
					background-color: #212529;
				}
				.Size-Change {
					height: 290px;
					width: 400px;
					position: relative;
					top: -102%;
					background-color: var(--base-color-green);
					border-radius: 25px;
					opacity: 0;
				}
				.Size-Change:hover {
					opacity: 0.5;
					transition: 0.3s;
				}
			}
		}
	}

	.Container {
		width: 100vw;
		height: 100vh;
		display: grid;
		place-items: center;
		position: absolute;
		z-index: 110;
		background-color: rgba(37, 37, 37, 0.8);
		.Information-Menu {
			width: 57vw;
			height: 95vh;
			display: grid;
			place-items: center;
			border-radius: 10px;
			background-color: var(--base-color-white);
		}
		.Title {
			height: 10vh;
			font-family: var(--base-font-bold);
			font-weight: 700;
			font-size: var(--bigx-font-size);
			color: var(--base-color-blue);
			text-transform: uppercase;
			padding-top: 5vh;
		}
		.sizePhoto {
			height: 53vh;
			width: 37vw;
			border-radius: 15px;
			padding-top: 5vh;
		}

		.Description {
			width: 37vw;
			display: grid;
			place-items: center;
			text-align: center;
			font-family: var(--base-font-bold);
			color: #212529;
		}
	}

	.Idk {
		.divider-custom {
			margin: 1.25rem 0 1.5rem;
			width: 100%;
			display: flex;
			justify-content: center;
			align-items: center;
			.divider-custom-line {
				width: 6vw;
				height: 0.5vh;
				background-color: var(--base-color-blue);
				border-radius: 5px;
			}
			.divider-custom-icon {
				width: 3.5vw;
				height: 3.5vh;
				display: flex;
				justify-content: center;
			}
			svg {
				color: var(--base-font-color-blue);
				width: 3.5vw;
				height: 3.5vh;
			}
		}
	}

	button {
		height: 5vh;
		width: 9vw;
		background-color: var(--base-color-green);
		color: var(--base-color-white);
		font-size: var(--base-font-bold);
		border: none;
		border-radius: 10px;
		display: flex;
		justify-content: center;
		align-items: center;
		transition: 0.5;
		.svg-x {
			height: 2vh;
			width: 2vw;
		}
	}

	button:hover {
		background-color: var(--darker-color-green);
		transition: 0.5s-;
	}
</style>

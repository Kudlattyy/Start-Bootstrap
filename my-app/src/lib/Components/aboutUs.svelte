<script lang="ts">
	import Portfolio from '$lib/Components/portfolio.svelte';
</script>

<body>
	<section class="AboutUs">
		<div class="Header">
			<div class="Tittle">ABOUT</div>
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
		<div class="Content">
			<div class="Description">
				<div class="Description-First">
					Freelancer is a free bootstrap theme created by Start Bootstrap. The download includes the
					complete source files including HTML, CSS, and JavaScript as well as optional SASS
					stylesheets for easy customization.
				</div>
				<div class="Description-Second">
					You can create your own custom avatar for the masthead, change the icon in the dividers,
					and add your email address to the contact form to make it fully functional!
				</div>
			</div>
		</div>
		<div class="Footer">
			<div class="Button">
				<button class="Download">Free Download!</button>
			</div>
		</div>
	</section>
	<slot />
</body>

<style lang="scss">
	.AboutUs {
		height: 70vh;
		width: 100%;
		background-color: var(--base-color-green);
		.Header {
			display: grid;
			place-items: center;
			.Tittle {
				height: 5vh;
				width: 60%;
				display: flex;
				justify-content: center;
				margin-top: 100px;
				font-size: var(--tittle-font-size);
				color: var(--base-font-color-white);
				font-family: var(--base-font-bold);
				font-weight: 700;
			}
		}
		.Content {
			display: flex;
			justify-content: center;
			.Description {
				height: 30vh;
				width: 40vw;
				display: flex;
				justify-content: center;
				color: var(--base-font-color-white);
				font-family: var(--base-font-bold);
				font-size: var(--base-font-size);
			}
		}
		.Footer {
			height: 10vh;
			width: 100%;
			display: flex;
			justify-content: center;
			.Download {
				height: 7vh;
				width: 23vh;
				background-color: var(--base-color-green);
				border: solid 2px #ffffff;
				border-radius: 10px;
				font-size: var(--base-font-size);
				color: var(--base-font-color-white);
			}
			.Download:hover {
				color: var(--base-font-color-black);
				background-color: var(--base-color-white);
				transition-duration: 2s;
			}
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
				background-color: var(--base-color-white);
				border-radius: 5px;
			}
			.divider-custom-icon {
				width: 3.5vw;
				height: 3.5vh;
				display: flex;
				justify-content: center;
			}
			svg {
				color: var(--base-font-color-white);
				width: 3.5vw;
				height: 3.5vh;
			}
		}
	}

</style>

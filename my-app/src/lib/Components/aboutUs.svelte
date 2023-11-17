<script lang="ts">
	import Portfolio from '$lib/Components/portfolio.svelte';
</script>

<body>
	<section class="AboutUs">
		<div class="Header">
			<div class="Tittle">ABOUT</div>
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
			display: flex;
			justify-content: center;
			.Tittle {
				height: 10vh;
				width: 60%;
				display: flex;
				justify-content: center;
				margin-top: 100px;
				font-size: var(--tittle-font-size);
				color: var(--base-font-color-white);
				font-family: var(--base-font-bold);
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
				font-family: var(--base-font-slim);
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
				color:	var(--base-font-color-white);
			}
			.Download:hover {
				color: var(--base-font-color-black);
				background-color: var(--base-color-white);
				transition-duration: 2s;
			}
		}
	}
</style>

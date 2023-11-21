<script>
	import Avatar from '$lib/Avatar.png';
</script>

<body>
	<section class="Title">
		<div class="Container">
			<div class="Header-Content">
				<div class="Header">
					<img class="Avatar" src={Avatar} alt="Guy-Icon" />
				</div>
				<div class="Content">
					<div class="Caption">START BOOTSTRAP</div>
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
							><!-- <i class="fas fa-star"></i> Font Awesome fontawesome.com -->
						</div>
						<div class="divider-custom-line" />
					</div>
					<div class="Description">Graphic Artist - Web Designer - Illustrator</div>
				</div>
			</div>
		</div>
		<slot />
	</section>
</body>

<style lang="scss">
	.Title {
		height: 80vh;
		width: 100%;
		background-color: var(--base-color-green);
		display: grid;
		place-items: center;
		.Container {
			height: 40vh;
			width: 50vw;
			display: grid;
			place-items: center;
		}
		.Header-Content {
			display: flex;
			flex-direction: column;
			justify-content: center;
			align-items: center;
		}

		.Content {
			display: flex;
			flex-direction: column;
			.Caption {
				padding-top: 25px;
				font-size: var(--mega-font-size);
				color: var(--base-font-color-white);
				font-family: var(--base-font-bold);
				font-weight: 700;
			}
			.Description {
				font-size: var(--base-font-size);
				color: var(--base-font-color-white);
				font-family: var(--base-font-bold);
				text-align: center;
			}
		}
	}

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

	.Avatar {
		height: 260px;
		widows: 270.55px;
	}

	@media (max-width: 768px) {
		.Title {
			height: 90vh;
			.Container {
				height: 60vh;
				width: 100vw;
			}
			.Header-Content {
				flex-direction: column;
			}
			.Content {
				.Caption {
					font-size: var(--bigger-font-size);
					display: flex;
					justify-content: center;
					width: 98vw;
					text-align: center;
				}
				.Description {
					font-size: var(--smaller-font-size);
				}
			}
		}
		.divider-custom {
			height: 5vh;
			.divider-custom-line {
				width: 30vw;
			}
			.divider-custom-icon {
				width: 10vw;
				height: 10vh;
			}
			svg {
				width: 10vw;
				height: 10vh;
			}
		}
		.Avatar {
			height: 260px;
		}
	}
</style>

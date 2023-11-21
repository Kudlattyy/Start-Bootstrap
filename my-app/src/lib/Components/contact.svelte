<script>
	let name = '';
	let email = '';
	let number = '';
	let message = '';
</script>

<body>
	<section class="contact">
		<div class="container">
			<div class="title">CONTACT ME</div>
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
			<div class="forms">
				<div class="form-group">
					<label for="name"><b>Full name </b></label>
					<input bind:value={name} type="text" id="name" />
				</div>

				<div class="form-group">
					<label for="email"><b>Email address </b></label>
					<input bind:value={email} type="text" id="email" />
				</div>

				<div class="form-group">
					<label for="number"><b> Phone number </b></label>
					<input bind:value={number} type="text" id="number" />
				</div>

				<div class="form-group">
					<label for="message"><b>Message </b></label>
					<textarea bind:value={message} rows="5" cols="50" id="message" />
				</div>

				<button class="submit">Send</button>
			</div>
		</div>
	</section>
	<slot />
</body>

<style lang="scss">
	.contact {
		min-height: 110vh;
		width: 100%;
		display: grid;
		place-items: center;
		background-color: var(--base-color-white);
	}

	.container {
		height: 90vh;
		width: 50vw;
		display: flex;
		flex-direction: column;
		align-items: center;
	}

	.title {
		font-size: var(--tittle-font-size);
		font-family: var(--base-font-bold);
		color: var(--base-font-color-blue);
		font-weight:  700;
	}

	.forms {
		height: 80vh;
		width: 50vw;
		padding-top: 5vh;
		font-family: var(--base-font-bold);
		font-size: var(--big-font-size);
		color: var(--font-color-grey);
		display: flex;
		flex-direction: column;
	}

	.form-group {
		margin-bottom: 20px;
	}

	.submit {
		margin-top: 2vh;
		height: 9vh;
		width: 7vw;
		background-color: var(--base-color-green);
		opacity: 0.75;
		border: none;
		border-radius: 10px;
		font-size: var(--button-font-size);
		font-family: var(--base-font-bold);
		color: var(--base-font-color-white);
	}

	input,
	textarea {
		border: none;
		outline: none;
		width: 100%;
		padding-top: 20px;
		border-bottom: 0.5px solid var(--input-color);
		font-size: var(--big-font-size);
		color: var(--base-font-color-black);
	}

	textarea {
		resize: vertical;
		overflow: auto;
		height: auto;
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
	@media (max-width: 768px) {
		
		.contact{
			height: 150vh;

		}
		.Idk{
			width: 100%;
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
	}
		}
</style>

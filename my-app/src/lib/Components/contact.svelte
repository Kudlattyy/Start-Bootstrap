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

<style>
	.contact {
		min-height: 100vh;
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
	}

	.forms {
		height: 80vh;
		width: 50vw;
		padding-top: 5vh;
		font-family: var(--base-font-slim);
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
</style>

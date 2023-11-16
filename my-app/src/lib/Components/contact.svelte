<body>
	<section class="Contact">
		<div class="Container">
			<div class="Title">CONTACT ME</div>
			<div class="Forms">
				<label for="name"><b>Full name </b><br /></label>
				<input type="text" name="name" id="name" /> <br /> <br />
				<label for="email"><b>Email address </b><br /></label>
				<input type="text" name="Email" id="Email" /> <br /> <br />
				<label for="name"><b> Phone number </b><br /></label>
				<input type="text" name="Number" id="Number" /> <br /> <br />
				<label for="Message"><b>Message </b><br /></label>
				<textarea rows="5" cols="50" name="messege" />
                <button class="Sumbit">Send</button>
			</div> 
		</div>
	</section>
	<slot />
</body>

<style lang="scss">
	.Contact {
		height: 100vh;
		width: 100%;
		display: grid;
		place-items: center;
		background-color: var(--base-color-white);
		.Container {
			height: 90vh;
			width: 50vw;
			display: flex;
			flex-direction: column;
			align-items: center;
			.Title {
				font-size: var(--tittle-font-size);
				font-family: var(--base-font-bold);
				color: var(--base-font-color-blue);
			}
			.Forms {
				height: 80vh;
				width: 50vw;
				padding-top: 5vh;
				font-family: var(--base-font-slim);
				font-size: var(--big-font-size);
				color: var(--font-color-grey);
                .Sumbit{
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
			}
		}
	}

	input {
		border: none;
		width: 100%;
		padding-top: 20px;
		border-bottom: 1px solid var(--font-color-grey);
	}

	textarea {
		border: none;
		width: 100%;
		padding-top: 20px;
		border-bottom: 1px solid var(--font-color-grey);
	}
</style>

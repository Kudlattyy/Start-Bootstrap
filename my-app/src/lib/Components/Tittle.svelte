<script>
	import Avatar from '$lib/Avatar.png';
</script>

<body>
	<div class="main">
		<div class="Container">
			<img src={Avatar} alt="Gostek" />
		</div>
	</div>
	<slot />
</body>

<style lang="scss">
	.main {
		height: 80vh;
		width: 100%;
		background-color: #1abc9c;
		display: flex;
		justify-content: center;
		align-items: center;
		flex-wrap: wrap;
		.Container {
			height: 80vh;
			width: 30vw;
			display: flex;
			justify-content: center;
			align-items: center;
		}
	}
</style>

<script>

	import Button from '$lib/components/button.svelte';
	import Profile from '$lib/components/profilePicture.svelte'

</script>

<svelte:head>
	<title>MrChileball Links</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<body>

	<Profile />
	
	<h1>@chileball</h1>
	<video autoplay loop muted class="background">
		<source src="https://motionbgs.com/media/2978/minecraft-sunset.960x540.mp4">
	</video>
	<div>
		<Button text="Minecraft Portfolio" link="https://chileballchile.crevado.com/portfolio"/>
	</div>
	<div>
		<Button text="Minecraft Hosting" link="https://panel.axonode.xyz"/>
	</div>
	<div>
		<Button text="Instagram" link="https://www.instagram.com/chileball.master/"/>
	</div>
	<div>
		<Button text="Instagram" link="https://www.instagram.com/chileball.master/"/>
	</div>
	<div>
		<Button text="dasd" link="https://www.instagram.com/chileball.master/"/>
	</div>
</body>


 
<style>
	body{
		padding-top: 2.5vh;
	}

	.background{
		width: 100vw;
		height: 100vh;
		object-fit: cover;
		position: fixed;
		left: 0;
		right: 0;
		top: 0;
		bottom: 0;
		z-index: -1;
		filter: blur(2px);
	}
	
</style>

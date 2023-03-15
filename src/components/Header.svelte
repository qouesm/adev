<script lang="ts">
	import Logo from '../assets/logo.png';
	import Button from './Button.svelte';
	import Icon from './Icon.svelte';

	// import { onMount } from 'svelte';
</script>

<div class="flex items-center justify-between px-16 py-6">
	<img class="h-12" src={Logo} alt="Logo" />
	<!-- <span class="flex gap-x-4"> -->
	<!--   <a href="/">Home</a> -->
	<!-- </span> -->
	<Button left href="mailto:andrew@andrewavella.dev"><Icon symbol="mail" />Contact</Button>
</div>

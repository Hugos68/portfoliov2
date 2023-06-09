<script lang='ts'>
	import '../theme.postcss';
	import '@skeletonlabs/skeleton/styles/skeleton.css';
	import '../app.postcss';
	
	import Footer from './Footer.svelte';
	import Header from './Header.svelte';
	import Main from './Main.svelte';
</script>

<Header />
<Main><slot /></Main>
<Footer />


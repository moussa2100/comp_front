<script>
	import '../app.css';
	import Header from '../component/header.svelte';
	import Footer from '../component/Footer.svelte';
	
	let { children } = $props();


</script>

<Header></Header>

{@render children()}

<Footer></Footer>
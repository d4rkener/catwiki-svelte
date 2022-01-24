<script>
	import Navbar from '../components/Navbar.svelte';
	import Footer from '../components/Footer.svelte';
	import '../scss/_boilerplate.scss';
</script>

<div class="container">
	<Navbar />
	<slot />
	<Footer />
</div>

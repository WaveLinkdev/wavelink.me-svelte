<script>
	import '@fontsource/jetbrains-mono';
	import '../style/global.css';
	import Navigation from './components/navigation.svelte';
  import Background from './components/background.svelte';
import Footer from './components/footer.svelte';
</script>

<Navigation />
<Background />

<div style="min-height: 100vh;">
  <slot/>
</div>

<Footer />
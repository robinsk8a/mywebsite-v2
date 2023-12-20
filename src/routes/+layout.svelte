<script>
  import '../golbal.css'
	import Header from "$lib/components/Header.svelte";
	import Footer from "$lib/components/Footer.svelte";

</script>


<Header />
<body>
  <slot />
</body>
<Footer />
<script lang="ts">
    import "../app.css";    
    
	import Footer from "./Footer.svelte";
    import Main from "./Main.svelte";
    import Header from "./Header.svelte";
</script>

<Header />
<Main><slot/></Main>
<Footer />
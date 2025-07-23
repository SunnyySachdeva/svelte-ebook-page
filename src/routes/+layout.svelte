<script lang="ts">
    import "./../app.css";
    import Header from "./header.svelte";
    import Footer from "./footer.svelte";
    let {children} = $props()
</script>

<!-- <Header /> -->
{@render children()}
<Footer />

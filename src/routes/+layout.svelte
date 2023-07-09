<script>
    import Header from "$lib/Header.svelte";
    import Footer from "$lib/Footer.svelte";
    // export const prerender = true;
</script>

<Header />
<main>
    <slot />
</main>
<Footer />

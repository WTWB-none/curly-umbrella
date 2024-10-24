<script>
    import Header from "./header.svelte";
    import MainSection from "./main_section.svelte";
    import Info from "./info.svelte";
</script>

<div id="app-container">
    <Header />
    <MainSection />
    <Info />
</div>

<style>
    #app-container {
        max-width: 100%;
        font-family: Arial, Helvetica, sans-serif;
        padding-left: 15%;
        padding-right: 15%;
        padding-top: 1.5%;
    }
</style>

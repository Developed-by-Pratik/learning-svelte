<script>
    import Header from "./Header.svelte";
    import Toggler from "./ToggleStatus.svelte"
    let name = "Pratik";
    let nameState = $state('John');
</script>

<!-- <Header name="Kartik" />
<Header {name} />
<Header name = {nameState} />

<input type="text" bind:value={nameState}> -->


<Toggler />
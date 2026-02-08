<script>
    import Header from "./Header.svelte";
    import Toggler from "./ToggleStatus.svelte"
    
    let name = "Pratik";
    let nameState = $state('John');

    let derivedName = $derived(name + " " + "Derived Name");

</script>

<!-- <Header name="Kartik" />
<Header {name} />
<Header name = {nameState} />
<input type="text" bind:value={nameState}> -->

<!-- <Header /> // This is throwing an error because we havent passed name prop
// So to make the prop optional we can give deafult value in child component -->


<Header name = {derivedName}/>
<input type="text" bind:value={derivedName}>

<!-- <Toggler /> -->


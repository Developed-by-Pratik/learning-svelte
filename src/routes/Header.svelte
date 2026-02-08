<script lang="ts">  
    let { name } : { name: String } = $props();
</script>

<h1>Hello {name}</h1>
<h3>Hello {name.length}</h3>

<style>
    h1 {
        color: red;
    }
</style>
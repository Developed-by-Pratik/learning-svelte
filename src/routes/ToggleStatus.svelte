<script lang="ts">
    let status : 'OPEN' | 'CLOSED' = $state('OPEN');
    let newStatus = $state("OPEN onclick");

    const toggle = () => {
        status = status === 'OPEN' ? 'CLOSED' : 'OPEN';
    }

    const onclick = () => {
        newStatus = newStatus === "OPEN onclick" ? "CLOSED onclick" : "OPEN onclick";
    }

</script>

<h1>Store is {status} {newStatus}</h1>
<button onclick={toggle} >Toggle Status</button>
<button {onclick} >Toggle Status onclick</button>

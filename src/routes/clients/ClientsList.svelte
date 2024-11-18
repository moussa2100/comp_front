<script>
    import ClientCard from './ClientCard.svelte';
  
    export let clients = [];
  </script>
  
  <div class="space-y-8">
    {#each clients as client}
      <ClientCard
        name={client.name}
        description={client.description}
        logo={client.logo}
      />
    {/each}
  </div>
  
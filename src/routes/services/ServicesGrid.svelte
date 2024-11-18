<script>
  export let services = []; // Receive the services array as a prop
</script>

<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
  {#each services as service}
    <div class="bg-white shadow-md rounded-md p-6">
      <h2 class="text-xl font-bold text-gray-800 mb-2">{service.title}</h2>
      <p class="text-gray-600 mb-4">{service.description}</p>
      <a href={service.link} class="text-yellow-500 font-medium hover:underline">
        Learn More →
      </a>
    </div>
  {/each}
</div>

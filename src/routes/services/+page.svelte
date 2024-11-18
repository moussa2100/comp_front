<script>
  import { onMount } from "svelte";
  import ServicesGrid from "./ServicesGrid.svelte";

  let services = []; // Initialize an empty array for services
  let loading = true; // Loading state
  let error = ""; // Error message

  // Fetch services from the API
  onMount(async () => {
    try {
      const response = await fetch("http://localhost:5000/api/services");
      if (response.ok) {
        services = await response.json(); // Update services with data from the API
      } else {
        throw new Error("Failed to fetch services.");
      }
    } catch (err) {
      error = err.message; // Set error message
      console.error(err);
    } finally {
      loading = false; // Turn off loading state
    }
  });
</script>

<section class="py-16 bg-gray-50 min-h-screen">
  <div class="container mx-auto text-center">
    <p class="text-yellow-500 font-medium uppercase mb-2">What We Do</p>
    <h1 class="text-4xl font-bold text-gray-900 mb-8">Services</h1>

    {#if loading}
      <!-- Loading Spinner -->
      <p>Loading services...</p>
    {:else if error}
      <!-- Error Message -->
      <p class="text-red-500">{error}</p>
    {:else}
      <!-- Services Grid -->
      <ServicesGrid {services} />
    {/if}
  </div>
</section>

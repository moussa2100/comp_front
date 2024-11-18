<script>
    import { onMount } from "svelte";
    import { goto } from "$app/navigation";
  
    let title = "";
    let subtitle = "";
    let message = "";
  
    // Fetch current hero content from the API
    const fetchHeroContent = async () => {
      try {
        const response = await fetch("http://localhost:5000/api/hero");
        if (!response.ok) throw new Error("Failed to fetch hero content.");
        const data = await response.json();
        title = data.title;
        subtitle = data.subtitle;
      } catch (error) {
        console.error(error);
        message = "Error loading hero content.";
      }
    };
  
    // Update hero content via API
    const updateHeroContent = async () => {
      try {
        const response = await fetch("http://localhost:5000/api/hero", {
          method: "POST",
          headers: {
            "Content-Type": "application/json",
          },
          body: JSON.stringify({ title, subtitle }),
        });
  
        if (!response.ok) throw new Error("Failed to update hero content.");
        message = "Hero content updated successfully!";
      } catch (error) {
        console.error(error);
        message = "Error updating hero content.";
      }
    };
  
    // Fetch hero content when the page loads
    onMount(fetchHeroContent);
  </script>
  
  <section class="py-16 bg-gray-100">
    <div class="container mx-auto max-w-lg">
      <h1 class="text-2xl font-bold mb-6">Admin Panel</h1>
  
      {#if message}
        <p class="mb-4 text-center text-green-600">{message}</p>
      {/if}
  
      <form
        on:submit|preventDefault={() => updateHeroContent()}
        class="space-y-4 bg-white p-6 shadow rounded"
      >
        <div>
          <label for="title" class="block text-sm font-medium text-gray-700">
            Title
          </label>
          <input
            id="title"
            type="text"
            bind:value={title}
            class="mt-1 block w-full border-gray-300 rounded-md shadow-sm focus:border-blue-500 focus:ring focus:ring-blue-200"
            required
          />
        </div>
  
        <div>
          <label for="subtitle" class="block text-sm font-medium text-gray-700">
            Subtitle
          </label>
          <textarea
            id="subtitle"
            bind:value={subtitle}
            class="mt-1 block w-full border-gray-300 rounded-md shadow-sm focus:border-blue-500 focus:ring focus:ring-blue-200"
            required
          ></textarea>
        </div>
  
        <div class="flex justify-between items-center">
          <button
            type="submit"
            class="bg-blue-600 text-white py-2 px-4 rounded hover:bg-blue-700"
          >
            Update
          </button>
          <a
            href="/"
            class="text-blue-600 hover:text-blue-800 transition underline"
          >
            Back to Home
          </a>
        </div>
      </form>
    </div>
  </section>
  
  <style>
    section {
      min-height: 100vh;
    }
  </style>
  
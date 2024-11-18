<script>
  import { onMount } from "svelte";
  let title = "Loading...";
  let subtitle = "Please wait...";

  // Fetch hero content from API
  onMount(async () => {
    const response = await fetch("http://localhost:5000/api/hero");
    const data = await response.json();
    title = data.title;
    subtitle = data.subtitle;
  });
</script>

<section class="bg-blue-50 relative">
  <div class="container mx-auto flex flex-col md:flex-row items-center py-12 px-6 md:py-20 md:px-12">
    <!-- Left Section: Text Content -->
    <div class="md:w-1/2 text-center md:text-left space-y-6">
 
      <h1 class="text-4xl md:text-6xl font-bold text-gray-800 leading-tight">
        {title}
      </h1>
      <p class="text-gray-600 text-lg">
        {subtitle}
      </p>
      <a
        href="#services"
        class="inline-block bg-blue-600 text-white px-6 py-3 rounded-md hover:bg-blue-700 transition-all font-medium"
      >
        Our Services →
      </a>
    </div>

    <!-- Right Section: Image -->
    <div class="md:w-1/2 mt-10 md:mt-0 relative">
      <div class="rounded-lg overflow-hidden shadow-lg">
        <img
          src="https://via.placeholder.com/500x400"
          alt="Business Consulting"
          class="w-full"
        />
      </div>
    </div>
  </div>
</section>

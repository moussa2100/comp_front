<script>
  let menuOpen = false;
</script>

<header class="bg-white border-b">
  <div class="container mx-auto flex justify-between items-center py-4 px-6">
    <!-- Left: Logo -->
    <div class="flex items-center space-x-2">
      <h1 class="text-blue-600 font-bold text-2xl">OmniVus.</h1>
      <p class="text-gray-500 text-sm">IT Service & Technology</p>
    </div>

    <!-- Middle: Navigation Links -->
    <nav class="hidden md:flex space-x-6">
      <a href="/" class="text-gray-700 hover:text-blue-600 font-medium">Home</a>
      <a href="/projects" class="text-gray-700 hover:text-blue-600 font-medium">Projects</a>
      <a href="/clients" class="text-gray-700 hover:text-blue-600 font-medium">Clients</a>
      <a href="/services" class="text-gray-700 hover:text-blue-600 font-medium">Services</a>
    </nav>

    <!-- Right: Contact Us Button -->
    <div class="flex items-center space-x-4">
      <button
        class="md:hidden focus:outline-none text-gray-700"
        on:click={() => (menuOpen = !menuOpen)}
        aria-label="Toggle menu"
      >
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="h-6 w-6"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M4 6h16M4 12h16M4 18h16"
          />
        </svg>
      </button>
      <a
        href="#contact"
        class="hidden md:inline-block bg-blue-600 text-white py-2 px-4 rounded-md hover:bg-blue-700 transition-all font-medium"
      >
        Contact Us →
      </a>
    </div>
  </div>

  <!-- Mobile Menu -->
  {#if menuOpen}
    <div class="md:hidden bg-white border-t">
      <nav class="flex flex-col items-center space-y-4 py-4">
        <a href="/" class="text-gray-700 hover:text-blue-600 font-medium">Home</a>
        <a href="/projects" class="text-gray-700 hover:text-blue-600 font-medium">Projects</a>
        <a href="/clients" class="text-gray-700 hover:text-blue-600 font-medium">Clients</a>
        <a href="/services" class="text-gray-700 hover:text-blue-600 font-medium">Services</a>
        <a href="/contact" class="text-gray-700 hover:text-blue-600 font-medium">Contact</a>
      </nav>
    </div>
  {/if}
</header>

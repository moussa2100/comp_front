<script>
    export let name;
    export let description;
    export let logo;
  </script>
  
  <div class="py-8 border-b border-gray-200 flex flex-col md:flex-row items-center md:items-start">
    <!-- Client Logo -->
    <div class="flex-shrink-0 mb-4 md:mb-0 md:mr-6">
      <img src={logo} alt="{name} Logo" class="w-32 h-auto object-contain" />
    </div>
  
    <!-- Client Info -->
    <div>
      <h2 class="text-2xl font-bold text-gray-800 mb-2">{name}</h2>
      <p class="text-gray-600 leading-relaxed">{description}</p>
    </div>
  </div>
  
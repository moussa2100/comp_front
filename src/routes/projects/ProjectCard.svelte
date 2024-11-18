<script>
    export let name;
    export let location;
    export let image;
  </script>
  
  <div class="p-4 bg-white rounded-lg shadow-lg transform hover:scale-105 transition duration-300">
    <img
      src={image}
      alt={name}
      class="w-full h-40 object-cover rounded-t-lg"
    />
    <div class="mt-4">
      <h3 class="text-xl font-semibold text-gray-800">{name}</h3>
      <p class="text-gray-600">{location}</p>
    </div>
  </div>
  
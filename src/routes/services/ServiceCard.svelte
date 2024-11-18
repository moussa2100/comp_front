<script>
    export let number;
    export let title;
    export let description;
    export let link = "#";
  </script>
  
  <div class="p-6 bg-white border rounded-lg shadow hover:shadow-lg transition duration-300">
    <div class="text-gray-300 text-4xl font-bold mb-4">{number}</div>
    <h3 class="text-xl font-bold text-gray-900 mb-2">{title}</h3>
    <p class="text-gray-600 mb-4">{description}</p>
    <a
      href={link}
      class="text-green-600 font-medium hover:underline flex items-center"
    >
      DETAILS →
    </a>
  </div>
  
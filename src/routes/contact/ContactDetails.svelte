<script>
    export let address = '1234 Omni Street, IT City, Saudi Arabia';
    export let phone = '+1-800-555-1234';
    export let mapSrc = 'https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d387190.2799144123!2d-74.25986584737497!3d40.69767006898707!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x89c24564f2a2c16f%3A0x92c8492c221a12b1!2sIT%20City%2C%20Saudi%20Arabia!5e0!3m2!1sen!2sus!4v1617172390982!5m2!1sen!2sus';
  </script>
  
  <div class="space-y-8">
    <div>
      <h3 class="text-xl font-bold text-gray-900">Our Address</h3>
      <p class="text-gray-600">{address}</p>
    </div>
    <div>
      <h3 class="text-xl font-bold text-gray-900">Call Us</h3>
      <p class="text-gray-600">{phone}</p>
    </div>
    <div>
      <h3 class="text-xl font-bold text-gray-900">Our Location</h3>
      <div class="overflow-hidden rounded-lg shadow-md">
        <iframe
          src={mapSrc}
          width="100%"
          height="300"
          style="border:0;"
          allowfullscreen=""
          loading="lazy"
          class="rounded-lg"
        ></iframe>
      </div>
    </div>
  </div>
  
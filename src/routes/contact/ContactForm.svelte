<script>
    let name = '';
    let email = '';
    let message = '';
  
    function sendEmail() {
      alert(`Email sent by ${name} (${email}): ${message}`);
      // Add email sending logic here (e.g., connect to an API).
    }
  </script>
  
  <form on:submit|preventDefault={sendEmail} class="space-y-4">
    <div>
      <label for="name" class="block text-sm font-medium text-gray-700">Name</label>
      <input
        id="name"
        type="text"
        bind:value={name}
        placeholder="Your Name"
        class="mt-1 block w-full p-3 border rounded-md bg-gray-50 text-gray-700 focus:outline-none focus:ring focus:ring-blue-200"
        required
      />
    </div>
    <div>
      <label for="email" class="block text-sm font-medium text-gray-700">Email</label>
      <input
        id="email"
        type="email"
        bind:value={email}
        placeholder="Your Email"
        class="mt-1 block w-full p-3 border rounded-md bg-gray-50 text-gray-700 focus:outline-none focus:ring focus:ring-blue-200"
        required
      />
    </div>
    <div>
      <label for="message" class="block text-sm font-medium text-gray-700">Message</label>
      <textarea
        id="message"
        bind:value={message}
        placeholder="Your Message"
        rows="4"
        class="mt-1 block w-full p-3 border rounded-md bg-gray-50 text-gray-700 focus:outline-none focus:ring focus:ring-blue-200"
        required
      ></textarea>
    </div>
    <button
      type="submit"
      class="w-full bg-blue-600 text-white py-3 rounded-md hover:bg-blue-700 transition"
    >
      Send Message
    </button>
  </form>
  
<script>
  import ContactForm from './ContactForm.svelte';
  import ContactDetails from './ContactDetails.svelte';
</script>

<section class="py-16 bg-gray-50 min-h-screen px-4 md:px-0">
  <div class="container mx-auto grid grid-cols-1 md:grid-cols-2 gap-12">
    <!-- Left: Contact Form -->
    <div>
      <h1 class="text-4xl font-bold text-gray-800 mb-8">Contact Us</h1>
      <ContactForm />
    </div>

    <!-- Right: Contact Details -->
    <div>
      <ContactDetails />
    </div>
  </div>
</section>

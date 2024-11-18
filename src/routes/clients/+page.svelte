<script>
    import ClientsList from './ClientsList.svelte';
  
    const clients = [
      {
        name: 'Royal Commission for Jubail and Yanbu',
        description:
          'The Royal Commission for Jubail and Yanbu was established as per a Royal Decree issued by HM King Khalid – May Allah have mercy upon him – in 21 September 1975 (16 Ramadan 1395H). The Royal Decree read “A Royal Commission shall be formed to execute the necessary infrastructure plan for the preparation of Jubail and Yanbu Cities as industrial areas. The Commission shall have an independent legal personality”. An independent budget was dedicated for the Royal Commission.',
        logo: 'https://via.placeholder.com/150x100?text=RCJY+Logo',
      },
      {
        name: 'Saudi Aramco',
        description:
          'Saudi Aramco is the state-owned oil company of the Kingdom of Saudi Arabia and a fully integrated, global petroleum and chemicals enterprise. Over the past 80 years they have become a world leader in hydrocarbons exploration, production, refining, distribution, and marketing.',
        logo: 'https://via.placeholder.com/150x100?text=Aramco+Logo',
      },
      // Add more clients as needed
    ];
  </script>
  
  <section class="py-16 bg-gray-50 min-h-screen">
    <div class="container mx-auto">
      <h1 class="text-4xl font-bold text-gray-800 mb-8 text-center">Clients</h1>
      <ClientsList {clients} />
    </div>
  </section>
  
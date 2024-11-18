<script>
    import ProjectsGrid from '../../routes/projects/ProjectsGrid.svelte';
  
    // Project data
    const projects = [
      {
        name: 'Modern Office',
        location: 'New York, USA',
        image: 'https://via.placeholder.com/300x200'
      },
      {
        name: 'Luxury Villa',
        location: 'Dubai, UAE',
        image: 'https://via.placeholder.com/300x200'
      },
      {
        name: 'Urban Apartment',
        location: 'Tokyo, Japan',
        image: 'https://via.placeholder.com/300x200'
      },
      {
        name: 'Beach House',
        location: 'Malibu, USA',
        image: 'https://via.placeholder.com/300x200'
      },
      // Add more projects as needed
    ];
  </script>
  
  <section class="py-16 bg-gray-50 min-h-screen">
    <div class="container mx-auto">
      <h1 class="text-4xl font-bold text-gray-800 mb-8 text-center">Our Projects</h1>
      <ProjectsGrid projects={projects} />
    </div>
  </section>
  
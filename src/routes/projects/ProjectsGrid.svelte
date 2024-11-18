<script>
    import ProjectCard from './ProjectCard.svelte';
  
    // Example data for projects
    export let projects = [];
  </script>
  
  <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6">
    {#each projects as project}
      <ProjectCard
        name={project.name}
        location={project.location}
        image={project.image}
      />
    {/each}
  </div>
  
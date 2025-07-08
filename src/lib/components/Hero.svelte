<!-- Hero.svelte -->
<script lang="ts">
  import Container from './ui/Container.svelte';
  import Button from './ui/Button.svelte';
</script>

<section class="relative bg-gradient-to-b from-blue-50 to-white py-20 sm:py-32">
  <Container>
    <div class="flex flex-col items-center text-center">
      <h1 class="text-4xl font-bold tracking-tight text-gray-900 sm:text-6xl">
        <slot name="title">Modern Transportation Solutions</slot>
      </h1>
      <p class="mt-6 text-lg leading-8 text-gray-600 max-w-2xl">
        <slot name="description">
          Experience luxury and comfort with our premium limousine services. Professional drivers, exceptional vehicles, and unmatched customer service.
        </slot>
      </p>
      <div class="mt-10 flex gap-x-6">
        <Button size="lg" onclick={() => window.location.href = '/contact'}>
          Get Started
        </Button>
        <Button size="lg" variant="outline" onclick={() => window.location.href = '/services'}>
          Learn More
        </Button>
      </div>
    </div>
  </Container>
</section>

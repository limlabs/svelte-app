<!-- Icons.svelte -->
<script lang="ts">
  // Common icon props
  export let size = 24;
  export let color = "currentColor";
  export let strokeWidth = 2;
  export let className = "";
  export let type: 'check' | 'arrow-right' | 'chevron-down' | 'phone' | 'mail' = 'check';
</script>

<svg xmlns="http://www.w3.org/2000/svg" width={size} height={size} viewBox="0 0 24 24" fill="none" stroke={color} stroke-width={strokeWidth} stroke-linecap="round" stroke-linejoin="round" class="inline-block align-middle {className}">
  {#if type === 'check'}
    <polyline points="20 6 9 17 4 12"></polyline>
  {:else if type === 'arrow-right'}
    <path d="M5 12h14"></path>
    <path d="m12 5 7 7-7 7"></path>
  {:else if type === 'chevron-down'}
    <path d="m18 15-6-6-6 6"/>
  {:else if type === 'phone'}
    <path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07 19.5 19.5 0 0 1-6-6 19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 4.11 2h3a2 2 0 0 1 2 1.72 12.84 12.84 0 0 0 .7 2.81 2 2 0 0 1-.45 2.11L8.09 9.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45 12.84 12.84 0 0 0 2.81.7A2 2 0 0 1 22 16.92z"></path>
  {:else if type === 'mail'}
    <rect width="20" height="16" x="2" y="4" rx="2"></rect>
    <path d="m22 7-8.97 5.7a1.94 1.94 0 0 1-2.06 0L2 7"></path>
  {/if}
</svg>

<style>
  svg {
    display: inline-flex;
    justify-content: center;
    align-items: center;
    vertical-align: -0.1875em;
    margin-left: -0.125em;
  }
</style>

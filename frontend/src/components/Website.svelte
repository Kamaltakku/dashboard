<script>
    export let name = "website name";
    export let url = "website url";
    export let src = "website pic";
    export let health;
</script>
{#if health === 0}
    <a href={url}
       class="flex items-center variant-filled-error p-3 text-base font-bold rounded-lg">
        <img {src} alt="This is a link to the favicon" class="object-scale-down h-8 w-8">
        <span class="flex-1 ml-3 whitespace-nowrap">{name}</span>
    </a>
{:else if health === 1}
    <a href={url}
       class="flex items-center variant-filled-warning p-3 text-base font-bold rounded-lg">
        <img {src} alt="This is a link to the favicon" class="object-scale-down h-8 w-8">
        <span class="flex-1 ml-3 whitespace-nowrap">{name}</span>
    </a>
{:else if health === 2}
    <a href={url}
       class="flex items-center variant-filled-success p-3 text-base font-bold rounded-lg">
        <img {src} alt="This is a link to the favicon" class="object-scale-down h-8 w-8">
        <span class="flex-1 ml-3 whitespace-nowrap">{name}</span>
    </a>
{/if}

<script>
    import Website from "./Website.svelte";
    export let groupName = "empty group name";
    export let description = "description empty";
    let links = [
        {name: "name1", url: "url1", src: "favicon.png", health: 1},
        {name: "name2", url: "url2", src: "favicon.png", health: 0},
        {name: "name3", url: "url3", src: "favicon.png", health: 1},
        {name: "name4", url: "url4", src: "favicon.png", health: 2},
        {name: "name5", url: "url5", src: "favicon.png", health: 1},
    ]
</script>

<div class="grid variant-filled-primary max-w-sm p-4 rounded-xl sm:p-6 shadow-2xl">
    <h5 class="mb-3">
        {groupName}
    </h5>
    <p class="text-sm font-normal">{description}</p>
    {#each links as link}
        <ul class="my-2">
            <li>
                <Website {...link}/>
            </li>
        </ul>
    {/each}
</div>


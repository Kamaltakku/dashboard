<script>
    import Website from "./Website.svelte";
    export let groupName = "empty group name";
    export let description = "description empty";
    let links = [
        {name: "name1", url: "url1", src: "ikona1"},
        {name: "name2", url: "url2", src: "ikona2"},
        {name: "name3", url: "url3", src: "ikona3"},
        {name: "name4", url: "url4", src: "ikona4"},
        {name: "name5", url: "url5", src: "ikona5"},
    ]
</script>

<div class="grid bg-surface-100-700-token w-full max-w-sm p-4 rounded-xl sm:p-6">
    <h5 class="mb-3">
        {groupName}
    </h5>
    <p class="text-sm font-normal">{description}</p>
    {#each links as link}
        <ul class="my-2 space-y-2 border rounded-token border-token">
            <li>
                <Website {...link}/>
            </li>
        </ul>
    {/each}
</div>


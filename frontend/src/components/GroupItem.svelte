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

<div class="w-full max-w-sm p-4 bg-white rounded-xl shadow sm:p-6 dark:bg-gray-800 dark:border-gray-700">
    <h5 class="mb-3 text-base font-semibold text-gray-900 md:text-xl dark:text-white">
        {groupName}
    </h5>
    <p class="text-sm font-normal text-gray-500 dark:text-gray-400">{description}</p>
    {#each links as link}
        <ul class="my-4 space-y-3">
            <li>
                <Website {...link}/>
            </li>
        </ul>
    {/each}
</div>


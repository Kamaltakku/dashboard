<script>
    import GroupItem from "../components/GroupItem.svelte";

    let owner = "Default owner"
    let items = [
        {groupName: "groupDevelopment", url: "urlDevelopment", src: "srcDevelopment", description: "development"},
        {groupName: "groupFun", url: "urlFun", src: "srcFun", description: "fun"},
        {groupName: "groupPersonal", url: "urlPersonal", src: "srcPersonal", description: "personal"}
    ];
</script>
<div class="h-screen grid bg-amber-800">
    <div class="title text-center text-5xl bg-blue-500 p-5">
        <h1>Welcome again, {owner}</h1>
    </div>
    <div class="bg-red-500 p-10">
        <div class="grid grid-cols-{items.length} ">
            {#each items as item (item.groupName)}
                <GroupItem {...item}/>
            {/each}
        </div>

    </div>
</div>



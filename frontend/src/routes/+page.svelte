<script>
    import GroupItem from "../components/GroupItem.svelte";
    import {AppShell} from "@skeletonlabs/skeleton";
    import DashboardHeader from "../components/DashboardHeader.svelte";

    let items = [
        {groupName: "groupDevelopment", url: "urlDevelopment", src: "srcDevelopment", description: "development"},
        {groupName: "groupFun", url: "urlFun", src: "srcFun", description: "fun"},
        {groupName: "groupPersonal", url: "urlPersonal", src: "srcPersonal", description: "personal"}
    ];
</script>
<AppShell>
    <svelte:fragment slot="header">
        <DashboardHeader/>
    </svelte:fragment>
    <slot>
        <div class="h-screen">
            <div class="grid justify-items-center p-10">
                <div class="grid shadow-2xl grid-cols-3 gap-2">
                    {#each items as item (item.groupName)}
                        <GroupItem {...item}/>
                    {/each}
                </div>

            </div>
        </div>
    </slot>
    <svelte:fragment slot="footer">
        <div class="">A ma footer</div>
    </svelte:fragment>

</AppShell>



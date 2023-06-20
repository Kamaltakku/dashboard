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
        <div class="grid auto-rows-max justify-items-center p-10 variant-filled-primary min-h-full">
            <div class="grid grid-cols-3 gap-20 rounded-xl">
                {#each items as item (item.groupName)}
                    <GroupItem {...item}/>
                {/each}
            </div>
        </div>
    </slot>
    <svelte:fragment slot="footer">
        <div class="variant-filled-primary">A ma footer</div>
    </svelte:fragment>

</AppShell>



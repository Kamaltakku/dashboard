<script>
    export let name = "website name";
    export let url = "website url";
    export let src = "website pic";
</script>
<div>
    <a href={url}
       class="flex items-center p-3 text-base font-bold rounded-lg">
        <img {src} alt="This is a link to the favicon">
        <span class="flex-1 ml-3 whitespace-nowrap">{name}</span>
    </a>
</div>

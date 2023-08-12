<script lang="ts">
    import { TableOfContents } from "@skeletonlabs/skeleton";
    import { page } from "$app/stores";
    

				
				
</script>

<aside
    class="fixed border-l pt-4 px-3 bg-gray-800 bg-opacity-50 border-neutral-700 h-full top-14 right-0 z-40 w-72"
    aria-label="Sidebar"
>
    {#key $page.url.pathname}
        <TableOfContents  label="Actions" target="#toc-target" />
    {/key}
</aside>

<div class="mr-72 p-4">
    <ol class="breadcrumb">
        <li class="crumb"><a class="anchor" href={$page.url.pathname}>{$page.url.pathname.toUpperCase()}</a></li>
    </ol>
    <slot />
</div>


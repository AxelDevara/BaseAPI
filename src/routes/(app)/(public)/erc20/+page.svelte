<script>

    import { CodeBlock } from "@skeletonlabs/skeleton";
    import { page } from "$app/stores";
</script>
<div id="toc-target">
    <h2 class="mt-4 h3 mb-3">Overview</h2>
    <hr />
    <p class="mt-3">A set of API endpoints to call erc-20 based read functions.</p>
    <CodeBlock language="Plaintext" code={$page.url.origin + "/public/v1/{action}"}></CodeBlock>
</div>

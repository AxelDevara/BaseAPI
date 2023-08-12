<script lang="ts">
    import { CodeBlock, Tab, TabGroup } from "@skeletonlabs/skeleton";
    import { page } from "$app/stores";
    import Chaintable from "$lib/component/chaintable.svelte";
    import Heading from "$lib/component/heading.svelte";
    let tabSetBalance: number = 0;
  </script>
  
  <div id="toc-target">
    <Heading text="Overview" />
    <p class="mt-3">
      A set of API endpoints to call erc-20 based read functions. Follow the
      format below to make a call
    </p>
    <CodeBlock
      language="Plaintext"
      code={$page.url.origin +
        "/public/v1/erc721/{contract address}/{action}?ChainID={ChainID}"}
    />
    <Chaintable />
    <Heading text="Balance" badge="POST" />
    <p class="mt-3">
      Get the balance of a contract that you own
    </p>
    <TabGroup>
      <Tab bind:group={tabSetBalance} name="tab1" value={0}>Javascript</Tab>
      <Tab bind:group={tabSetBalance} name="tab2" value={1}>C#</Tab>
      <Tab bind:group={tabSetBalance} name="tab3" value={2}>C++</Tab>
      <!-- Tab Panels --->
      <svelte:fragment slot="panel">
        {#if tabSetBalance === 0}
          <CodeBlock
            language="js"
            code={`const response = await fetch('http://example.com/movies.json');`}
          />
        {:else if tabSetBalance === 1}
          <CodeBlock
            language="c#"
            code={`var response = await client.GetAsync(uri);`}
          />
        {:else if tabSetBalance === 2}
          <CodeBlock language="java" code={`URL url = new URL("http://example.com");
          HttpURLConnection con = (HttpURLConnection) url.openConnection();
          con.setRequestMethod("GET");`} />
        {/if}
      </svelte:fragment>
    </TabGroup>
  
    <Heading text="TotalSupply" badge="GET"/>
    <Heading text="Symbol" badge="GET" />
    <Heading text="URL" badge="GET" />
  </div>
  
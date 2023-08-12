<script lang="ts">
  import {
    Table,
    tableMapperValues,
    type TableSource,
  } from "@skeletonlabs/skeleton";

  const chainData = [
    { position: 1, name: "Optimism", id: 10 },
    { position: 2, name: "Optimism Testnet", id: 420 },
    { position: 3, name: "Zora", id: 7777777 },
    { position: 4, name: "Base", id: 8453 },
    { position: 5, name: "Base Testnet", id: 84531 },
  ];

  const table: TableSource = {
    // A list of heading labels.
    head: ["Name", "Chain ID"],
    // The data visibly shown in your table body UI.
    body: tableMapperValues(chainData, ["name", "id"]),
  };
</script>

<Table class="rounded-lg" regionHeadCell="bg-neutral-700" regionBody="bg-neutral-800" source={table} />

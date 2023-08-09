<script>
    import { JSONEditor, Mode } from "svelte-jsoneditor";

    let content = {
        text: "{}", // can be used to pass a stringified JSON document instead
    };
</script>

<div class="px-4">
    <p
        class="inline-flex justify-between items-center py-1 px-1 pr-4 mb-5 text-sm text-blue-700 bg-blue-100 rounded-full dark:bg-blue-900 dark:text-blue-300 hover:bg-blue-200 dark:hover:bg-blue-800"
    >
        <span
            class="text-xs bg-blue-600 rounded-full text-white px-4 py-1.5 mr-3"
            >Demo</span
        >
        <span class="text-sm font-medium"
            >Proof of concept work to show you what's possible</span
        >
    </p>
    <h1
        class="mb-2 text-2xl font-extrabold tracking-tight leading-none text-gray-900 md:text-5xl lg:text-4xl dark:text-white"
    >
        Create Your Own API Under In 5 Minutes
    </h1>
    <div class="my-json-editor jse-theme-dark">
        <JSONEditor mode={Mode.text} mainMenuBar={false} navigationBar={false} bind:content />
    </div>
</div>

<style>
    /* load one or multiple themes */
    @import "svelte-jsoneditor/themes/jse-theme-dark.css";
</style>

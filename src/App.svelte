<script lang="ts">
  import { getResponderUuid } from "@formsort/custom-question-api";
  import { onMount } from "svelte";

  let responderUuid: string;
  let status: string;
  onMount(async () => {
    status = "loading";
    try {
      responderUuid = await getResponderUuid();
      status = "loaded";
    } catch (e) {
      status = `failed: ${e.toString()}`;
    }
  });
</script>

<main>
  <p>status: ({status}), your responder: {responderUuid}</p>
</main>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>

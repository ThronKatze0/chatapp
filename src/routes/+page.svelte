<script lang="ts">
  import { Card, Input } from "flowbite-svelte";
  import { collectionStore } from "sveltefirets";

  const messagesStore = collectionStore<string>("chats/public/messages");
</script>

<div class="flex justify-center items-center space-y-4 min-h-screen">
  <Card size="lg" padding="xl">
    <h1 class="text-2xl font-bold">wsefwsef</h1>
    <div class="flex flex-col min-h-full">
      {#each $messagesStore as message}
        <div>{message}</div>
      {/each}
    </div>
    <Input id="large-input" size="lg" placeholder="Message" />
  </Card>
</div>

<script lang="ts">
  import { cn } from "$lib/utils";

  export let img!: string;
  export let name: string;
  export let username!: string;
  export let body!: string;
  export let stack!: string;
  export let link: string = ""; // 🔗 pass this as prop
</script>

<figure
  on:click={() => window.open(link, "_blank")}
  class={cn(
    "relative cursor-pointer overflow-hidden rounded-2xl border p-4 transition hover:shadow-md w-120",
    // light styles
    "border-gray-950/[.1] bg-gray-950/[.01] hover:bg-gray-950/[.05]",
    // dark styles
    "dark:border-gray-50/[.1] dark:bg-gray-50/[.10] dark:hover:bg-gray-50/[.15]"
  )}
>
  <div class="flex flex-row items-center gap-2">
    <img class="rounded-full" width="32" height="32" alt="" src={img} />
    <div class="flex flex-col">
      <figcaption class="text-sm font-medium dark:text-white">
        {name}
      </figcaption>
      <p class="text-xs font-medium dark:text-white/40">{username}</p>
    </div>
  </div>
  <blockquote class="mt-2 text-sm text-justify">{body}</blockquote>
  <blockquote class="mt-2 text-sm text-justify">{stack}</blockquote>
</figure>

<script lang="ts">
  import { cn } from "$lib/utils";

  export let shimmerColor = "#ffffff";
  export let shimmerSize = "0.05em";
  export let shimmerDuration = "5s";
  export let borderRadius = "8px";
  export let background = "rgba(0, 0, 0, 1)";
  export let href: string | null = null;
  let className: any = "";
  export { className as class };
</script>

{#if href}
  <a
    {href}
    target={href.startsWith("http") ? "_blank" : "_self"}
    rel={href.startsWith("http") ? "noopener noreferrer" : undefined}
    style:--spread="90deg"
    style:--shimmer-color={shimmerColor}
    style:--radius={borderRadius}
    style:--speed={shimmerDuration}
    style:--cut={shimmerSize}
    style:--bg={background}
    class={cn(
      "group relative z-0 flex cursor-pointer items-center justify-center overflow-hidden whitespace-nowrap border border-white/10 px-6 py-3 text-white [background:var(--bg)] [border-radius:var(--radius)] dark:text-white",
      "transform-gpu transition-transform duration-300 ease-in-out active:translate-y-[1px]",
      className
    )}
  >
    <!-- shimmer layers -->
    <div
      class={cn(
        "-z-30 blur-[2px]",
        "absolute inset-0 overflow-visible [container-type:size]"
      )}
    >
      <div
        class="absolute inset-0 h-[100cqh] animate-magicslide [aspect-ratio:1] [border-radius:0] [mask:none]"
      >
        <div
          class="animate-spin-around absolute inset-[-100%] w-auto rotate-0 [background:conic-gradient(from_calc(270deg-(var(--spread)*0.5)),transparent_0,var(--shimmer-color)_var(--spread),transparent_var(--spread))] [translate:0_0]"
        ></div>
      </div>
    </div>

    <slot>Shimmer Link</slot>

    <!-- highlight -->
    <div
      class={cn(
        "insert-0 absolute h-full w-full",
        "rounded-m px-4 py-1.5 text-sm font-medium shadow-[inset_0_-8px_10px_#ffffff1f]",
        "transform-gpu transition-all duration-300 ease-in-out",
        "group-hover:shadow-[inset_0_-6px_10px_#ffffff3f]",
        "group-active:shadow-[inset_0_-10px_10px_#ffffff3f]"
      )}
    ></div>

    <!-- backdrop -->
    <div
      class={cn(
        "absolute -z-20 [background:var(--bg)] [border-radius:var(--radius)] [inset:var(--cut)]"
      )}
    ></div>
  </a>
{:else}
  <button
    style:--spread="90deg"
    style:--shimmer-color={shimmerColor}
    style:--radius={borderRadius}
    style:--speed={shimmerDuration}
    style:--cut={shimmerSize}
    style:--bg={background}
    class={cn(
      "group relative z-0 flex cursor-pointer items-center justify-center overflow-hidden whitespace-nowrap border border-white/10 px-6 py-3 text-white [background:var(--bg)] [border-radius:var(--radius)] dark:text-white",
      "transform-gpu transition-transform duration-300 ease-in-out active:translate-y-[1px]",
      className
    )}
  >
    <!-- shimmer layers -->
    <div
      class={cn(
        "-z-30 blur-[2px]",
        "absolute inset-0 overflow-visible [container-type:size]"
      )}
    >
      <div
        class="absolute inset-0 h-[100cqh] animate-magicslide [aspect-ratio:1] [border-radius:0] [mask:none]"
      >
        <div
          class="animate-spin-around absolute inset-[-100%] w-auto rotate-0 [background:conic-gradient(from_calc(270deg-(var(--spread)*0.5)),transparent_0,var(--shimmer-color)_var(--spread),transparent_var(--spread))] [translate:0_0]"
        ></div>
      </div>
    </div>

    <slot>Shimmer Button</slot>

    <!-- highlight -->
    <div
      class={cn(
        "insert-0 absolute h-full w-full",
        "rounded-m px-4 py-1.5 text-sm font-medium shadow-[inset_0_-8px_10px_#ffffff1f]",
        "transform-gpu transition-all duration-300 ease-in-out",
        "group-hover:shadow-[inset_0_-6px_10px_#ffffff3f]",
        "group-active:shadow-[inset_0_-10px_10px_#ffffff3f]"
      )}
    ></div>

    <!-- backdrop -->
    <div
      class={cn(
        "absolute -z-20 [background:var(--bg)] [border-radius:var(--radius)] [inset:var(--cut)]"
      )}
    ></div>
  </button>
{/if}

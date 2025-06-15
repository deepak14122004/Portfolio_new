<script lang="ts">
    let { children}  = $props();
    import { onMount } from "svelte";

  
    import "../app.css";
    import { ModeWatcher } from "mode-watcher";
   
    import type { Snippet } from "svelte";
  

  </script>
  
  <ModeWatcher />

    <div class="h-screen w-screen">
      {@render children()}
    </div>

  
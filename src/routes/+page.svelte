<script lang="ts">
  import { buttonVariants } from "$lib/components/ui/button/index.js";
  import * as Tooltip from "$lib/components/ui/tooltip/index.js";

  const sides: ("top" | "bottom" | "left" | "right")[] = ["top", "bottom", "left", "right"];
</script>

<div class="flex flex-wrap gap-8">
    {#each sides as side}
        <Tooltip.Provider>
            <Tooltip.Root>
                <Tooltip.Trigger class={buttonVariants({ variant: "outline" })}>{side}</Tooltip.Trigger>
                <Tooltip.Content side={side}>
                    <p>Add to library</p>
                </Tooltip.Content>
            </Tooltip.Root>
        </Tooltip.Provider>
    {/each}
</div>

<script lang="ts">
  import { flip } from 'svelte/animate'
  import { dndzone, type DndEvent } from 'svelte-dnd-action'
  import CommingSoon from './CommingSoon.svelte'
  import Box1 from './Box1.svelte'
  import type { ComponentType } from 'svelte'

  function elasticOut(stifness: number, damping: number) {
    return (t: number) => {
      const D = Math.sqrt(stifness - Math.pow(damping, 2))
      return (
        1 +
        Math.pow(1 - Math.sqrt(t), damping) * ((damping / D) * Math.sin(D * t) - Math.cos(D * t))
      )
    }
  }

  type Box = {
    id: number
    component: ComponentType
  }

  let boxes: Box[] = [
    { id: 1, component: Box1 },
    { id: 2, component: CommingSoon },
    { id: 3, component: CommingSoon },
    { id: 4, component: CommingSoon },
    { id: 5, component: CommingSoon },
    { id: 6, component: CommingSoon }
  ]

  function handleDnd(e: CustomEvent<DndEvent<Box>>) {
    boxes = e.detail.items
  }
</script>

<main>
  <nav>
    <h1>Welcome to Uika Website</h1>
  </nav>
  <div
    use:dndzone={{ items: boxes, flipDurationMs: 300 }}
    on:consider={handleDnd}
    on:finalize={handleDnd}
    class="boxes"
  >
    {#each boxes as box (box.id)}
      <div
        animate:flip={{ duration: d => Math.sqrt(d) * 600, easing: elasticOut(500, 9) }}
        class="box"
      >
        <svelte:component this={box.component} />
      </div>
    {/each}
  </div>
</main>

<style>
  .boxes {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: repeat(2, 1fr);
    height: 100vh;
    background-color: var(--color-red);
    gap: 20px;
    position: relative;
    padding: 20px;
  }

  .box {
    border-radius: 20px;
    background-color: var(--color-bg-card);
    position: relative;
    overflow: hidden;
  }
</style>

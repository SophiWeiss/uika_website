<script lang="ts">
  export let length: number = 10
</script>

<div>
  {Array.from({ length })
    .map(() => 'Comming Soon')
    .join(' • ')}
</div>

<style>
  div {
    display: block;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%) rotate(-30deg);
    background-color: var(--color-bg-accent-variant);
    color: var(--color-text-accent-variant);
    text-align: center;
    padding: 5px 0;
    font-weight: bold;
    overflow: hidden;
    white-space: nowrap;
    pointer-events: none;
  }
</style>

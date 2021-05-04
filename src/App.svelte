<script>
  import ScatterPlot from './components/ScatterPlot.svelte';

  const xySet = [
    {
      x: 0,
      y: 1
    },
    {
      x: 2,
      y: 3
    },
    {
      x: 5,
      y: 10
    },
    {
      x: 10,
      y: 8
    },
    {
      x: 12,
      y: 7
    },
  ];
</script>

<ScatterPlot
  xySet={xySet}
/>

<style>
</style>

<script>
  import embed from 'vega-embed';

  export let xySet;

  const spec = {
    $schema: 'https://vega.github.io/schema/vega-lite/v5.json',
    width: 'container',
    height: 'container',
    mark: {
      type: 'point', // line
      shape: 'diamond',
      filled: true,
      size: 300
    },
    encoding: {
      x: {
        field: 'x',
        type: 'quantitative',
        title: 'x values'
      },
      y: {
        field: 'y',
        type: 'quantitative',
        title: 'y values'
      }
    }
  };

  let container;

  $: if (xySet) embed(container, {
    ...spec,
    data: { values: xySet}
  });
</script>

<div class="scatter-plot-container">
  <div
    class="scatter-plot"
    bind:this={container}
  >
  </div>
</div>

<style>
  .scatter-plot-container {
    width: 100%;
    height: 100%;
  }

  .scatter-plot-container > div {
    width: 800px;
    height: 600px;
  }
</style>
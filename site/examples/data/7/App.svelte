<script>
  import * as Pancake from "@sveltejs/pancake";

  const sourceData = [10, 2, 4, 9, 14, 12, 5, 8, 9];

  const data = sourceData.map((item, i) => ({ x: i, y: item }));
  const vertMaxVal = Math.max(null, ...sourceData) + 2;
  const barWidth = 0.95; // or use border-left for a more consistent result
  const xAxisTickCount = data.length; // approximate
  const xAxisAdjustment = -0.5;
</script>

<style>
  .chart {
    height: 300px;
    width: 600px;
    padding: 3em 2em 2em 3em;
    box-sizing: border-box;
  }

  .axes {
    width: 100%;
    height: 100%;
    border-left: 1px solid black;
    border-bottom: 1px solid black;
    opacity: 0.6;
  }

  .label {
    opacity: 0.6;
  }

  .y.label {
    position: absolute;
    left: -2.5rem;
    width: 2rem;
    text-align: right;
    bottom: -0.5em;
  }

  .x.label {
    position: absolute;
    width: 4rem;
    left: -2rem;
    bottom: -2rem;
    font-family: sans-serif;
    text-align: center;
  }

  .column {
    height: 100%;
    background-color: #1f77b4;
  }
</style>

<div class="chart">
  <Pancake.Chart
    x1={xAxisAdjustment}
    x2={data.length - 1}
    y1={0}
    y2={vertMaxVal}>
    <Pancake.Box
      x1={xAxisAdjustment}
      x2={data.length + xAxisAdjustment}
      y2={vertMaxVal}>
      <div class="axes" />
    </Pancake.Box>

    <Pancake.Grid vertical count={xAxisTickCount} let:value>
      <span class="x label">{value}</span>
    </Pancake.Grid>

    <Pancake.Grid horizontal count={3} let:value>
      <span class="y label">{value}</span>
    </Pancake.Grid>

    <Pancake.Columns {data} width={barWidth}>
      <div class="column" />
    </Pancake.Columns>
  </Pancake.Chart>
</div>

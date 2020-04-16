<script>
  import * as Pancake from "@sveltejs/pancake";

  const points = [
    { x: 0, y: 0 },
    { x: 1, y: 1 },
    { x: 2, y: 4 },
    { x: 3, y: 9 },
    { x: 4, y: 16 },
    { x: 5, y: 25 },
    { x: 6, y: 36 },
    { x: 7, y: 49 },
    { x: 8, y: 64 },
    { x: 9, y: 81 },
    { x: 10, y: 100 }
  ];
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
  }

  .y.label {
    position: absolute;
    left: -2.5em;
    width: 2em;
    text-align: right;
    bottom: -0.5em;
  }

  .x.label {
    position: absolute;
    width: 4em;
    left: -2em;
    bottom: -22px;
    font-family: sans-serif;
    text-align: center;
  }

  path.data {
    stroke: red;
    stroke-linejoin: round;
    stroke-linecap: round;
    stroke-width: 2px;
    fill: none;
  }
</style>

<div class="chart">
  <Pancake.Chart x1={0} x2={10} y1={0} y2={100}>
    <Pancake.Box x2={10} y2={100}>
      <div class="axes" />
    </Pancake.Box>

    <Pancake.Grid vertical count={5} let:value>
      <span class="x label">{value}</span>
    </Pancake.Grid>

    <Pancake.Grid horizontal count={3} let:value>
      <span class="y label">{value}</span>
    </Pancake.Grid>

    <Pancake.Svg>
      <Pancake.SvgLine data={points} let:d>
        <path class="data" {d} />
      </Pancake.SvgLine>
    </Pancake.Svg>
  </Pancake.Chart>
</div>

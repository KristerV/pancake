<script>
  import Chart1 from "./1/App.svelte";
  import Chart2 from "./2/App.svelte";
  import Chart3 from "./3/App.svelte";
  import Chart4 from "./4/App.svelte";
  import Chart5 from "./5/App.svelte";
  import Chart6 from "./6/App.svelte";
  import Chart7 from "./7/App.svelte";
</script>

<style>
  header {
    display: flex;
    justify-content: space-between;
    align-items: baseline;
    border-bottom: 1px solid rgba(255, 62, 0, 0.2);
    margin: 0 0 1em 0;
    padding: 0 0 3px 0px;
    overflow: hidden;
  }

  h3 {
    /*border-bottom: 3px solid #ddd;*/
    margin: 0;
    line-height: 1;
  }

  .chart-preview {
    margin: 2em 0 6em 0;
  }

  p {
    margin: 0;
    line-height: 1;
  }

  a {
    font-size: 14px;
    color: #ff3e00;
    border-bottom: 6px solid rgba(255, 62, 0, 0.2);
    text-decoration: none;
  }
</style>

<div class="chart-preview">
  <header>
    <h3>Line Chart</h3>
    <p>
      <a
        href="https://svelte.dev/repl/8cde242924fa4bc993dd7b3ec14640ab?version=3.20.1">
        Edit
      </a>
    </p>
  </header>
  <Chart6 />
</div>

<div class="chart-preview">
  <header>
    <h3>Bar Chart</h3>
    <p>
      <a
        href="https://svelte.dev/repl/cd2d467a3cfd405ca7cae22800d922e6?version=3.20.1">
        Edit
      </a>
    </p>
  </header>
  <Chart7 />
</div>

<div class="chart-preview">
  <header>
    <h3>Population pyramid</h3>
    <p>
      <a href="https://svelte.dev/repl/8686ac654dff448eafbe7cb396b8a058">
        Edit
      </a>
    </p>
  </header>
  <Chart1 />
</div>

<div class="chart-preview">
  <header>
    <h3>Life expectancy</h3>
    <p>
      <a href="https://svelte.dev/repl/3eaa39931e8045cf87da8b482e502c29">
        Edit
      </a>
    </p>
  </header>
  <Chart2 />
</div>

<div class="chart-preview">
  <header>
    <h3>Treemap</h3>
    <p>
      <a href="https://svelte.dev/repl/2a8acd2328ff4a5398def8b8c8252904">
        Edit
      </a>
    </p>
  </header>
  <Chart3 />
</div>
<div class="chart-preview">
  <header>
    <h3>Stacked to Grouped Bars</h3>
    <p>
      <a
        href="https://svelte.dev/repl/34bce599eb744d66b80073d21a67bdc2?version=3.18.1">
        Edit
      </a>
    </p>
  </header>
  <Chart4 />
</div>
<div>
  <header>
    <h3>Slope Graph</h3>
    <p>
      <a
        href="https://svelte.dev/repl/c99280af92464455bb4fa522403bf06a?version=3.18.2">
        Edit
      </a>
    </p>
  </header>
  <Chart5 />
</div>

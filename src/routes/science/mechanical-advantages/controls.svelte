<script>
  let {
    load = $bindable(),
    effortArm = $bindable(),
    loadArm = $bindable()
  } = $props()
</script>

<div class="controls">
  <label>
    Load
    <input type="range" min="10" max="200" step="10" bind:value={load} />
    <span>{load} N</span>
  </label>

  <label>
    Effort arm
    <input type="range" min="0.2" max="2" step="0.1" bind:value={effortArm} />
    <span>{effortArm} m</span>
  </label>

  <label>
    Load arm
    <input type="range" min="0.1" max="1.5" step="0.1" bind:value={loadArm} />
    <span>{loadArm} m</span>
  </label>
</div>
<script>
  let { load, effort, mechanicalAdvantage } = $props()
</script>

<div class="formula">
  <h2>Mechanical Advantage</h2>
  <p>MA=Load ÷ Effort</p>
  <p>
    MA={load} ÷ {effort.toFixed(1)}
  </p>
  <strong>MA={mechanicalAdvantage.toFixed(2)}×</strong>
</div>
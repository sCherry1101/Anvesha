<script>
  let { load, effortArm, loadArm }=$props()
  let effort=$derived((load*loadArm)/effortArm)
  let mechanicalAdvantage=$derived(load/effort)
  let totalLength=$derived(effortArm+loadArm
  let loadPosition=$derived((effortArm/totalLength)*100)
</script>

<div class="lever">
  <div class="lever__scene">
    <div
      class="lever__bar"
      style={`--load-position: ${loadPosition}%`}
    >
      <div class="lever__load">
        <span>{load} N</span>
        <div class="weight"></div>
      </div>

      <div class="lever__fulcrum"></div>

      <div class="lever__effort">
        <span>{effort.toFixed(1)} N</span>
        <div class="weight"></div>
      </div>

    </div>

  </div>

  <div class="lever__values">

    <div>
      <span>Load</span>
      <strong>{load} N</strong>
    </div>

    <div>
      <span>Effort</span>
      <strong>{effort.toFixed(1)} N</strong>
    </div>

    <div>
      <span>Mechanical Advantage</span>
      <strong>{mechanicalAdvantage.toFixed(2)}×</strong>
    </div>

  </div>

</div>

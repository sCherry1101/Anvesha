<script>
  let { load, effort, effortArm, loadArm }=$props()

  let loadTorque=$derived(load*loadArm)
  let effortTorque=$derived(effort*effortArm)

  let mechanicalAdvantage=$derived(load/Math.max(effort,0.01))

  let torqueDifference=$derived(effortTorque-loadTorque)

  let angle=$derived(
    Math.max(-15,Math.min(15,torqueDifference/loadTorque*15))
  )
</script>

<div class="lever">

  <div class="lever__scene">

    <div
      class="lever__bar"
      style={`transform:translate(-50%,-50%) rotate(${angle}deg)`}
    >

      <div class="lever__load">
        <span>{load} N</span>
        <div class="weight"></div>
      </div>

      <div class="lever__effort">
        <span>{effort} N</span>
        <div class="weight"></div>
      </div>

    </div>

    <div class="lever__fulcrum"></div>

  </div>

  <div class="lever__values">

    <div>
      <span>Load</span>
      <strong>{load} N</strong>
    </div>

    <div>
      <span>Effort</span>
      <strong>{effort} N</strong>
    </div>

    <div>
      <span>Mechanical Advantage</span>
      <strong>{mechanicalAdvantage.toFixed(2)}×</strong>
    </div>

    <div>
      <span>Load Torque</span>
      <strong>{loadTorque.toFixed(1)} Nm</strong>
    </div>

    <div>
      <span>Effort Torque</span>
      <strong>{effortTorque.toFixed(1)} Nm</strong>
    </div>

  </div>

</div>


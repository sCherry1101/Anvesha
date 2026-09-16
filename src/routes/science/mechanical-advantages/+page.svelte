<script>
  import '$lib/assets/stylesheet/global.css'
  import '$lib/assets/stylesheet/layout.css'
  import Controls from './controls.svelte'
  import Formula from './formula.svelte'
  import Lever from './lever.svelte'
  import './style.css'

  let load = $state(100)
  let effortArm = $state(1)
  let loadArm = $state(0.2)

  let effort = $derived((load * loadArm) / effortArm)
  let mechanicalAdvantage = $derived(load / effort)
</script>

<section class="mechanical-advantage">

  <article class="mechanical-advantage__simulation">

    <h1>Mechanical Advantage</h1>

    <p>
      Explore how a lever can multiply force by changing the position
      of the fulcrum.
    </p>

    <Lever
      {load}
      {effortArm}
      {loadArm}
    />

  </article>

  <aside class="mechanical-advantage__controls">

    <Controls
      bind:load
      bind:effortArm
      bind:loadArm
    />

    <Formula
      {load}
      {effort}
      {mechanicalAdvantage}
    />

  </aside>

</section>
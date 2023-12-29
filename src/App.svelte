<script>
  import Slider from "./Slider.svelte";
  let red = 100;
  let green = 150;
  let blue = 70;
</script>

<div class="container">
  <h1>Color Picker</h1>
  <div class="row">
    <div class="column">
      <form>
        <Slider colorName={"Red"} bind:colorValue={red} />
        <Slider colorName={"Green"} bind:colorValue={green} />
        <Slider colorName={"Blue"} bind:colorValue={blue} />
      </form>
    </div>
  </div>
  <div class="row">
    <div style="width: 100%; text-align:center">
      <h3>rgb ({red},{green},{blue})</h3>
    </div>
  </div>
  <div class="row">
    <div
      class="color-result"
      style="background-color: rgb({red},{green},{blue}"
    />
  </div>
</div>

<style>
  .color-result {
    width: 100%;
    height: 300px;
  }
</style>

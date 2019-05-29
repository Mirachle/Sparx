<template>
  <div style="text-align: center;">
    <div class="size-selected">Size</div>
    <select class="minimal">
      <option value="">Select</option>
      <option value="36">36</option>
      <option value="37">37</option>
      <option value="38">38</option>
      <option value="39">39</option>
      <option value="40">40</option>
      <option value="41">41</option>
      <option value="42">42</option>
      <option value="43">43</option>
      <option value="44">44</option>
      <option value="45">45</option>
    </select>
  </div>
</template>


<script>
export default {
  name: 'SizeInput',
  data() {
    return {};
  },
};
</script>


<style scoped>
.size-selected{
  font-family: Helvetica;
  font-size: 20px;
  font-weight: 300;
  font-style: normal;
  font-stretch: normal;
  line-height: 0.95;
  letter-spacing: normal;
  color: #111111;
  margin-bottom:3vh;
  display: inline-block;
}

select {

  /* styling */
  background-color: white;
  border-radius: 11px;
  border: solid 1px #979797;
  display: inline-block;
  font: inherit;
  padding: 0.2em 2em 0.2em 0.5em;
  margin-left: 1vw;
  color: black;

  /* reset */

  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
  -webkit-appearance: none;
  -moz-appearance: none;
}

select.minimal {
  background-image:
    linear-gradient(45deg, transparent 50%, gray 50%),
    linear-gradient(135deg, gray 50%, transparent 50%);
  background-position:
    calc(100% - 20px) calc(0.9em),
    calc(100% - 15px) calc(0.9em);
  background-size:
    5px 5px,
    5px 5px;
  background-repeat: no-repeat;
}
</style>

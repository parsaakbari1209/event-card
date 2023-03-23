<script lang="ts">
  export let heading: string
  export let styles: {
    background: string
    rotation: string
    translationX: string
    translationY: string
  }
  $: cssVarStyles = Object.entries(styles)
    .map(([key, value]) => `--${key}:${value}`)
    .join(';')
</script>

<div style={cssVarStyles}>
  <h1>{heading}</h1>
  <p>
    Rent <span>any</span> <span class="circle-letter">P</span> <span>Proof Collective</span> NFT for <span>1 day</span>
    for <span>0.05 ETH</span>
  </p>
</div>

<style>
  .circle-letter {
    align-items: center;
    background-color: #000;
    border-radius: 50%;
    box-sizing: border-box;
    display: flex;
    height: 20px;
    justify-content: center;
    width: 20px;
  }
  div {
    background-color: var(--background);
    border-radius: 5px;
    display: flex;
    flex-direction: column;
    font-family: Arial;
    height: 120px;
    justify-content: space-between;
    position: absolute;
    transform: rotate(var(--rotation)) translate(var(--translationX), var(--translationY));
    width: 300px;
  }
  h1 {
    color: #333;
    font-size: 15px;
    font-weight: 700;
    height: 30px;
    margin: 10px;
  }
  p {
    color: #333;
    display: flex;
    font-size: 10px;
    font-weight: 400;
    height: 20px;
    justify-content: space-around;
    margin: 10px;
  }
  span {
    color: #fff;
  }
  @media screen and (min-width: 500px) {
    .circle-letter {
      height: 22px;
      width: 22px;
    }
    div {
      height: 150px;
      width: 400px;
    }
    h1 {
      font-size: 20px;
      font-weight: 700;
    }
    p {
      font-size: 14px;
      font-weight: 400;
    }
  }
</style>

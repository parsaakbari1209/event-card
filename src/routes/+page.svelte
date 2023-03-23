<script lang="ts">
  import Card from '../lib/Card.svelte'
  const cards = [
    {
      heading: 'Expecting an airdrop this summer Board Apache and other stuff...',
      styles: { background: '#44eab1', rotation: '6deg', translationX: '0px', translationY: '-86px' },
    },
    {
      heading: 'Want to buy a ticket to VeeCon?',
      styles: { background: '#ff790f', rotation: '0deg', translationX: '-29px', translationY: '-43px' },
    },
    {
      heading: 'Want to preview the PROOF Discord before buying a membership?',
      styles: { background: '#9d97e0', rotation: '-9deg', translationX: '0px', translationY: '0px' },
    },
  ]
</script>

<svelte:head>
  <title>Event Cards</title>
</svelte:head>

<div>
  {#each cards as card}
    <Card heading={card.heading} styles={card.styles} />
  {/each}
</div>

<style>
  :global(body) {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }
  div {
    align-items: center;
    display: flex;
    height: 100vh;
    justify-content: center;
  }
</style>

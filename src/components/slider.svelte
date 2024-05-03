<script>
  export let cards = [
    {id:1,zoom:false,src:'',alt:'',text:''}
  ]
  export let num = '1';
</script>

<div class="slider">
  <div class="cards">
    {#each cards as card}
      <div class="content">
        <div class="image">
          <img src={card.src} alt={card.alt} draggable="false" class="select-none" class:zoom={card.zoom}>
        </div>
        <div class="text">
          {@html card.text}
        </div>
      </div>
    {/each}

    <div class="bullets">
      {#each cards as card}
        {#if card.id == 1}
        <div class="controls">
          <label>
            <input type="radio" name={`slider${num}`} class={`card${card.id}`} checked>
          </label>
        </div>
        {:else}
        <div class="controls">
          <label>
            <input type="radio" name={`slider${num}`} class={`card${card.id}`}>
          </label>
        </div>
        {/if}
      {/each}
    </div>
  </div>
  
</div>

<style>
  .slider {
    display: flex;
    justify-content: center;
  }
  .cards {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    align-items: flex-end;
    width: 300px;
    height: 480px;
    border: 3px solid black;
    border-radius: 15px;
    position: relative;
  }
  .content {
    display: none;
    flex-wrap: wrap;
    justify-content: center;
    align-items: flex-end;
    height: 90%;
  }
  .content .image {
    display: flex;
    height: 60%;
    padding: 5%;
  }
  .image img {
    object-fit: contain;
  }
  .image img.zoom {
    transition: scale 0.25s ease-in-out;
  }
  .image img.zoom:hover,
  .image img.zoom:active {
    z-index: 1;
    scale: 1.5;
  }
  @media all and (min-width:500px) {
    .image img.zoom:hover,
    .image img.zoom:active {
      z-index: 1;
      scale: 2;
    }  
  }
  .content .text {
    height: 40%;
  }
  .bullets {
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    width: 100%;
    height: 10%;
  }

  .bullets input {
    width: 1.5rem;
    height: 1.5rem;
    cursor: pointer;
    /* Add if not using autoprefixer */
    -webkit-appearance: none;
    appearance: none;
    /* For iOS < 15 to remove gradient background */
    background-color: #fff;
    border: 2px solid var(--yellow);
    border-radius: 50%;
    display: grid;
    place-content: center;
  }

  .bullets input::before {
    content: '';
    width: 0.75rem;
    height:0.75rem;
    border-radius: 50%;
    box-shadow: inset 1rem 1rem var(--blue);
    /* background-color: var(--yellow); */
    visibility: hidden;
    opacity: 0;
    scale: 0;
    transition: opacity 0.1s linear;
    transition: scale 0.2s ease-in-out;
  }

  .bullets input:checked::before {
    visibility: visible;
    opacity: 1;
    scale: 1;
  }

  .bullets input:focus-visible {
    outline: 2px solid black;
    outline-offset: 0px;
  }

  .controls label::before {
    display: none;
    position: absolute;
    top: 50%;
    width: 3rem;
    height: 3rem;
    font-size: 2rem;
    justify-content: center;
    align-items: center;
    background-color: #ccc;
    border-radius: 50%;
    opacity: 0.4;
  }
  .controls label:hover::before {
    opacity: 1;
  }
  
  .bullets:has(.card1:checked) .controls:nth-child(2) label::before,
  .bullets:has(.card2:checked) .controls:nth-child(3) label::before,
  .bullets:has(.card3:checked) .controls:nth-child(4) label::before,
  .bullets:has(.card4:checked) .controls:nth-child(5) label::before,
  .bullets:has(.card5:checked) .controls:nth-child(1) label::before {
    display: block;
    content: '>';
    right: -25%;
  }
  .bullets:has(.card1:checked) .controls:nth-child(5) label::before,
  .bullets:has(.card2:checked) .controls:nth-child(1) label::before,
  .bullets:has(.card3:checked) .controls:nth-child(2) label::before,
  .bullets:has(.card4:checked) .controls:nth-child(3) label::before,
  .bullets:has(.card5:checked) .controls:nth-child(4) label::before {
    display: block;
    content: '<';
    left: -25%;
  }

  .slider:has(.card1:checked) .cards .content:nth-child(1) {
    display: flex;
  }
  .slider:has(.card2:checked) .cards .content:nth-child(2) {
    display: flex;
  }
  .slider:has(.card3:checked) .cards .content:nth-child(3) {
    display: flex;
  }
  .slider:has(.card4:checked) .cards .content:nth-child(4) {
    display: flex;
  }
  .slider:has(.card5:checked) .cards .content:nth-child(5) {
    display: flex;
  }
</style>
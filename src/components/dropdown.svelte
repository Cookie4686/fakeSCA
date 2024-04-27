<li class="dropdown dropdown-bottom dropdown-end">
  <div role="button" tabindex="0" class="dropdown-btn">
    <label class="cursor-pointer">
      Dropdown
      <input type="checkbox" hidden/>
      <span class="dropdown-arrow">
        <svg class="inline align-baseline" width="16" height="16" viewBox="0 0 24 24" fill="white"><path d="M18 8v3.8l-6 4.6-6-4.6V8l6 4.6L18 8Z" fill="currentColor"></path></svg>
      </span>
    </label>
  </div>
  <ul class="dropdown-content z-[1] shadow w-max">
    <li><a href="/">Item 1</a></li>
    <li><a href="/">Item 2</a></li>
  </ul>
</li>

<style>
  .dropdown {
    position: relative;
    display: inline-block;
  }

  .dropdown-content {
    position: absolute;
    display: none;
  }

  .dropdown:has(input:checked) .dropdown-content {
    display: block;
  }


  /* Arrow animation */
  .dropdown-arrow svg {
    transition: 0.2s;
  }
  .dropdown:has(input:checked) .dropdown-arrow svg {
    transform: rotate(180deg);
    scale: 1.2;
  }
  
  /* Desktop */
  @media all and (min-width:768px) {
    .dropdown-content {
      border-radius: 0.5rem;
      padding: 0.5rem;
      z-index: 1;
    }
    .dropdown:has(input:checked) .dropdown-content,
    .dropdown:hover .dropdown-content,
    .dropdown:focus .dropdown-content,
    .dropdown:focus-within .dropdown-content {
      display: block;
    }
    .dropdown:has(input:checked) .dropdown-arrow svg,
    .dropdown:hover .dropdown-arrow svg,
    .dropdown:focus .dropdown-arrow svg,
    .dropdown:focus-within .dropdown-arrow svg {
      transform: rotate(180deg);
    }

    /* Dropdown Content Position Modifier */
    .dropdown-bottom .dropdown-content {
      bottom: auto;
      top: 100%;
      transform-origin: top;
    }
    .dropdown-end .dropdown-content {
      inset-inline-end: 0px;
    }
    /* .dropdown-end.dropdown-right .dropdown-content {
      bottom: 0px;
      top: auto;
    }
    .dropdown-end.dropdown-left .dropdown-content {
      bottom: 0px;
      top: auto;
    } */
  }




/* 
  @media all and (max-width:767px){
    .dropdown .dropdown-content li a {
      font-size: 1rem;
    }
    .dropdown,
    .dropdown:has(input:checked) .dropdown-content {
      display: flex;
      flex-wrap: wrap;
			justify-content: center;
			width: 100%;
      gap: 1.5rem;
    }
  }
  
  @media all and (min-width:767px){
    .dropdown {
      position: relative;
      display: inline-block;
    }
    .dropdown .dropdown-content {
      position: absolute;
      display: none;
      opacity: 0;
      width: max-content;
      padding: 1rem;
      transition: all 0.3s;
      border-radius: 10px;
      background-color: white;
      box-shadow: 5px 5px 15px #f2f2f2,-5px -5px 15px #fafafa;
    }
    .dropdown-bottom .dropdown-content {
      bottom: auto;
      top: 100%;
      transform-origin: top;
    }
    .dropdown .dropdown-content > * {
      padding: 0.5rem 0;
    }
  }
   */

</style>
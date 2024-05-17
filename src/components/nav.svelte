<script>
  import logo from '$lib/assets/SCAlogo2023_small.png'
  import { base } from '$app/paths';

  const links = [
    {text:'Home',href:'/home/'},
    {dropdown:true,text:'About',contents:[
      {text:'General Information',href:`${base}/about/`},
      {text:'Our vision',href:`${base}/about/vision/`},
      {text:'School History',href:`${base}/about/history/`},
      {text:'Management Board',href:`${base}/about/management/`}
    ]},
    {text:'Contact',href:`${base}/contact/`},
    {text:'Admission',href:`${base}/`},
    {text:'Others',dropdown:true,dropdown_end:true,contents:[
      {text:'Albums',href:`${base}/`},
      {text:'Donate',href:`${base}/donate/`},
      {text:'Student Council',href:`${base}/`}
    ]},
  ]
</script>

<nav class="flex fixed h-20 w-full p-4 z-10">
	<input type="checkbox" id="menubtn" hidden/>
	<!-- Logo-->
	<div class="logo relative w-max h-12 flex items-center">
    <div class="flex items-center h-full select-none">
      <img
      src={logo}
      alt="SCA logo"
      class="h-full"
      draggable="false"
			/>
			<span class="px-4 whitespace-nowrap">Sammuk Christian Academy</span>
		</div>
    <button class="menubtn absolute right-0">
      <label for="menubtn">
        <div class="bar1"></div>
        <div class="bar2"></div>
        <div class="bar3"></div>
      </label>
    </button>
	</div>
	<!-- Main Link -->
	<ul class="link select-none hidden">
    {#each links as link}
      {#if link.dropdown}
        <li class="dropdown dropdown-bottom" class:dropdown-end={link.dropdown_end}>
          <div role="button" tabindex="0" class="dropdown-btn">
            <label class="flex cursor-pointer">
              {link.text}
              <input type="checkbox" name="dropdown" hidden/>
              <span class="dropdown-arrow">
                <svg class="inline align-baseline" width="16" height="16" viewBox="0 0 24 24" fill="white"><path d="M18 8v3.8l-6 4.6-6-4.6V8l6 4.6L18 8Z" fill="currentColor"></path></svg>
              </span>
            </label>
          </div>
          <ul class="dropdown-content z-[1] shadow w-max">
            {#each link.contents as content}
              <li><a href={content.href}>{content.text}</a></li>
            {/each}
          </ul>
        </li>
      {:else}
        <li><a href={link.href}>{link.text}</a></li>
      {/if}
    {/each}
	</ul>
</nav>

<style>
	nav {
		background-color: black;
		transition: all 0.4s;
	}
  /* Dropdown */
  .dropdown {
    position: relative;
    display: inline-block;
  }
  .dropdown-content {
    display: none;
  }
  .dropdown:has(input:checked) .dropdown-content {
    display: block;
  }
  .dropdown-arrow svg {
    transition: 0.2s;
  }
  .dropdown:has(input:checked) .dropdown-arrow svg {
    transform: rotate(180deg);
    scale: 1.2;
  }
  @media all and (min-width:1049px) {
    .dropdown-content {
      position: absolute;
      border-radius: 0.5rem;
      padding: 0.5rem;
      z-index: 1;
      background-color: var(--primary);
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
    .dropdown-bottom .dropdown-content {
      bottom: auto;
      top: 100%;
      transform-origin: top;
    }
    .dropdown-end .dropdown-content {
      inset-inline-end: 0px;
    }
    .dropdown-end .dropdown-content li {
      display: flex;
      justify-content: end;
    }
  }
  @media all and (max-width:1050px) {
    .dropdown .dropdown-content li a {
      font-size: 1rem;
    }
    .dropdown,
    .dropdown:has(input:checked) .dropdown-content {
      display: flex;
      flex-wrap: wrap;
			justify-content: center;
			width: 100%;
      gap: 1rem;
    }
  }

	/* Tablet and Mobiles */
	@media all and (max-width: 1049px) {
		nav {
			color: white;
		}
   .logo {
      width: 100%;
    }
    .link li a, .link li.dropdown .dropdown-btn {
      font-size: 1.5rem;
      text-align: center;
      padding: 0.5rem 0;
    }
    nav:has(#menubtn:checked) {
      overflow: scroll;
    }
		nav:has(#menubtn:checked) {
			height: 100%;
			flex-wrap: wrap;
			gap: 0;
			align-content: flex-start;
		}
		nav:has(#menubtn:checked) .link {
			display: flex;
			flex-wrap: wrap;
			justify-content: center;
			width: 100%;
			padding-top: 3rem;
      gap: 1.5rem;
			position: relative;
		}
		nav:has(#menubtn:checked) .link li {
			width: 100%;
			display: flex;
			justify-content: center;
			flex-wrap: wrap;
		}

		/* Menu Button */
		.menubtn {
			--menu-btn-size: 2rem;
			cursor: pointer;
		}
		nav .menubtn .bar1,
		nav .menubtn .bar3 {
			width: var(--menu-btn-size);
			height: calc(var(--menu-btn-size) * 0.375);
			border-radius: var(--menu-btn-size);
			background-color: var(--yellow);
			transition: all 0.3s ease-in-out;
		}
		nav .menubtn .bar2 {
			height: calc(var(--menu-btn-size) * 0.125);
		}
		nav:has(#menubtn:checked) .menubtn .bar1 {
			transform: translateY(calc(var(--menu-btn-size) * 0.25)) rotate(225deg);
			background-color: var(--red);
		}
		nav:has(#menubtn:checked) .menubtn .bar3 {
			transform: translateY(calc(var(--menu-btn-size) * -0.25)) rotate(-45deg);
			background-color: var(--red);
		}
	}

	/* Desktop */
	@media all and (min-width: 1050px) {
		nav {
      justify-content: space-between;
			background-color: transparent;
		}
		nav .link {
			display: flex;
			justify-content: end;
			align-items: center;
			gap: 3rem;
		}
		nav .link a {
			display: inline;
			padding: 0;
			font-size: 1rem;
			color: black;
			white-space: nowrap;
		}
		nav .menubtn {
			display: none;
		}
	}

  /* Desktop link animations */
  @media all and (min-width: 1050px) {
    nav .link a {
      position: relative;
    }
    nav .link a::before {
      content: '';
      position: absolute;
      inset: 0;
      width: 0;
      background-color: var(--yellow);
      z-index: -1;
      transition: width 0.5s;
    }
    nav .link a::after {
      content: '';
      position: absolute;
      inset: auto auto -1px 0;
      width: 0;
      height: 1px;
      background-color: var(--blue);
      z-index: -1;
      transition: width 0.25s;
    }
  
    nav .link a:focus {
      outline: none;
    }
  
    nav .link a:focus-visible::before,
    nav .link a:hover::after,
    nav .link a:focus::after {
      width: 100%;
    }
  }

  /* Tablets & Mobile */
  @media all and (max-width:1049px){
    nav:has(#menubtn:checked) .link li {
			width: 100%;
			display: flex;
			justify-content: center;
			flex-wrap: wrap;
		}
  }
 </style>
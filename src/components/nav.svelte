<nav class="flex fixed h-20 w-full p-4 z-10">
	<input type="checkbox" class="hidden" id="menubtn" />
	<!-- Logo & NavButton -->
	<div class="logo relative w-full h-12 flex items-center">
		<div class="flex items-center h-full select-none">
			<img
				src="/src/public/SCAlogo2023_small.png"
				alt="SCA logo"
				class="h-full"
				draggable="false"
			/>
			<span class="px-4">Sammuk Christian Academy</span>
		</div>
		<label class="menubtn absolute right-0" for="menubtn">
			<div class="bar1"></div>
			<div class="bar2"></div>
			<div class="bar3"></div>
		</label>
	</div>

	<!-- Main Link -->
	<ul class="link select-none hidden overflow-hidden">
		<li><a href="/">Home</a></li>
		<li><a href="/about/">About</a></li>
		<li><a href="/">Contact</a></li>
		<li><a href="/">Donate</a></li>
		<li><a href="/">Student Council</a></li>
		<li><a href="/">Albums</a></li>
		<li><a href="/">Admission</a></li>
		<!-- <li class="dropdown">
      <button tabindex="0" class="dropdown-btn inline-flex items-center">
        Services
        <span class="dropdown-arrow ml-2">
          <svg class="inline align-baseline" width="16" height="16" viewBox="0 0 24 24" fill="white"><path d="M18 8v3.8l-6 4.6-6-4.6V8l6 4.6L18 8Z" fill="currentColor"></path></svg>
        </span>
      </button>
      
      <ul class="dropdown-content">
        <li><a href="/service/">All Services</a></li>
        <li><a href="/">Event Calendar</a></li>
        <li><a href="/">Food Rating</a></li>
      </ul>
    </li> -->
	</ul>
</nav>

<style>
	nav {
		background-color: black;
		transition: all 0.4s;
	}

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
		outline-offset: 4px;
	}

	nav .link a:focus::before,
	nav .link a:hover::after,
	nav .link a:focus::after {
		width: 100%;
	}

	/* Tablet and Mobiles */
	@media all and (max-width: 767px) {
		nav {
			color: white;
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
			position: relative;
		}
		nav:has(#menubtn:checked) .link li {
			width: 100%;
			display: flex;
			justify-content: center;
			flex-wrap: wrap;
		}
		nav:has(#menubtn:checked) .link li a {
			font-size: 1.5rem;
			text-align: center;
			padding: 1rem 0;
		}

		/* Menu Button */
		nav:has(#menubtn:checked) .menubtn .bar1 {
			transform: translateY(calc(var(--menu-btn-size) * 0.25)) rotate(225deg);
			background-color: var(--red);
		}
		nav:has(#menubtn:checked) .menubtn .bar3 {
			transform: translateY(calc(var(--menu-btn-size) * -0.25)) rotate(-45deg);
			background-color: var(--red);
		}
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
	}

	/* Desktop */
	@media all and (min-width: 768px) {
		nav {
			background-color: transparent;
		}
		nav .logo {
			width: 50%;
			justify-content: start;
		}
		nav .link {
			display: flex;
			width: 50%;
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

	/* Dropdown */
	/* .dropdown-arrow {
    display: flex;
    transition: 0.2s;
  }
  .dropdown:hover .dropdown-arrow,
  .dropdown:focus .dropdown-arrow,
  .dropdown:focus-within .dropdown-arrow {
    transform: rotate(180deg);
  }
  @media all and (max-width:767px){
    #menubtn:checked ~ nav .dropdown-btn {
      width: 100%;
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
    }
    #menubtn:checked ~ nav .dropdown-btn, .dropdown-content li {
      font-size: 1.5rem;
      text-align: center;
      color: white;
      padding: 1rem 0;
    }
    #menubtn:checked ~ nav .dropdown-btn {
      position: relative;
    }
    .dropdown .dropdown-content {
      height: 0;
      overflow: hidden;
      transition: all 0.6s;
    }
    .dropdown:focus .dropdown-content,
    .dropdown:focus-within .dropdown-content {
      height: 300px;
    }
    #menubtn:checked ~ nav .dropdown-arrow {
      position: absolute;
      right: 0;
    }
  }
  @media all and (min-width:767px){
    .dropdown {
      position: relative;
      display: inline-block;
    }
    .dropdown .dropdown-content {
      position: absolute;
      visibility: hidden;
      opacity: 0;
      transform-origin: top;
      width: max-content;
      padding: 1rem;
      transition: all 0.3s;
      border-radius: 10px;
      background-color: white;
      box-shadow: 5px 5px 15px #f2f2f2,-5px -5px 15px #fafafa;
    }
    .dropdown .dropdown-content > * {
      padding: 0.5rem 0;
    }
    .dropdown:hover .dropdown-content,
    .dropdown:focus .dropdown-content,
    .dropdown:focus-within .dropdown-content {
      visibility: visible;
      opacity: 1;
    }
  }
 */
</style>

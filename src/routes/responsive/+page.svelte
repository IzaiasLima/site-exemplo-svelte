<body class="container">
	<nav class="container">
		<ul>
			<li class="logo"><a href="/">BRAND</a></li>
		</ul>
		<input class="menu-btn" type="checkbox" id="menu-btn" />
		<label class="menu-icon" for="menu-btn">
			<span class="nav-icon" style="font-size: 1.8em">&#x2261;</span>
		</label>
		<ul class="menu">
			<li class="item"><a href="/">Home</a></li>
			<li class="item"><a href="/apis">API</a></li>
			<li class="item"><a href="/dialog">Dialog</a></li>
			<li class="item button"><a href="#top">Login</a></li>
			<li class="item button secondary"><a href="#top">Sign Up</a></li>
		</ul>
	</nav>
	<header>
		<h1>Menu Responsivo</h1>
	</header>

	<main class="container">
		<div>
			Alterar a dimensões da tela para testar a responsividade. O menu normal deve ser substituído
			pelo menu hamburg.
		</div>
	</main>
</body>

<style>
	body > header {
		/* usefule when "position: fixed" is turned-on */
		padding-top: 80px;
	}

	nav.container {
		/* background-color: var(--background-color); */
		position: fixed;
		/* remove the 'flex-direction' to move menu to the right */
		/* flex-direction: row-reverse; */
		z-index: 1;
		overflow: hidden;
		align-items: center;
	}

	nav :is(.menu-btn, .menu-icon) {
		display: none;
		cursor: pointer;
		user-select: none;
	}

	@media (max-width: 662px) {
		nav.container {
			max-width: 85vw;
			padding: 0;
			flex-wrap: wrap;
		}

		nav.container .menu-icon {
			display: block;
		}

		nav.container > ul.menu {
			flex-direction: column;
			align-items: flex-start;
			width: 100%;
			max-height: 0;
			border-radius: var(--border-radius);
			transition: max-height 0.3s ease-out;
			box-shadow: 0px 3px 8px;
			margin: 10px 10px;
			background-color: var(--background-color);
		}

		nav.container > ul.menu li {
			width: 100%;
		}
		nav.container > ul.menu a {
			padding-left: 20px;
			display: block;
		}
		nav.container > ul.menu a:hover {
			background-color: yellow;
		}

		nav.container .menu-btn:checked ~ .menu {
			max-height: 100vh;
		}
	}
</style>

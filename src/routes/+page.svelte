<script>
  import Footer from "$lib/components/Footer.svelte";
  import Navbar from "$lib/components/Navbar.svelte";
</script>

<body>
  <Navbar />

  <!-- Hero -->
  <div class="hero" data-theme="dark">
    <header class="container">
      <hgroup>
        <h1>About the Company</h1>
        <h2>A classic company or blog layout with a sidebar</h2>
      </hgroup>
      <p><a href="/" role="button">Call to action</a></p>
    </header>

    <small>
      <a
        href="https://br.freepik.com/psd-gratuitas/3d-logo-mockup-modern-facade-chrome-sign_9550645.htm#query=fachada%20de%20empresa&position=2&from_view=search&track=ais"
        >Imagem de asylab
      </a> no Freepik
    </small>
  </div>
  <!-- ./ Hero -->

  <!-- Main -->
  <main class="container">
    <div class="grid">
      <section>
        <hgroup>
          <h2>Ut sit amet sem ut velit</h2>
          <h3>Quisque mi est</h3>
        </hgroup>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque
          lobortis est vel velit bibendum ultrices. Sed aliquam tortor vel odio
          fermentum ullamcorper eu vitae neque. Sed non diam at tellus venenatis
          viverra.
        </p>
        <figure>
          <img
            src="img/ashim-d-silva-3Ijt7UkSBYE-unsplash-1500x750.jpg"
            alt="Architecture"
          />
          <figcaption>
            Image from
            <a href="https://unsplash.com/photos/3Ijt7UkSBYE" target="_blank"
              >unsplash.com</a
            >
          </figcaption>
        </figure>
        <h3>Nulla augue metus</h3>
        <p>
          Pacilisis sed ante ut, posuere volutpat quam. Maecenas maximus blandit
          mi ac finibus. Proin quis lacinia tellus. Aliquam erat volutpat.
          Aliquam erat volutpat. Phasellus suscipit nisi augue, id accumsan
          tortor auctor ut. Duis odio arcu, egestas nec nulla vel, fermentum
          bibendum ex.
        </p>
        <h3>Sed purus sapien, porta a cursus sed, maximus et metus.</h3>
        <p>
          Phasellus molestie ante sed massa bibendum, eget tempus ex
          sollicitudin. Vestibulum libero nulla, porttitor nec faucibus et,
          scelerisque eget quam. Nullam finibus tempor dui, vel congue urna
          condimentum ac. Fusce ultricies mauris justo, nec vulputate mauris
          pulvinar eu. Sed tempus ligula lorem, at tincidunt risus mollis non.
        </p>
      </section>

      <aside>
        <a href="/" aria-label="Example"
          ><img
            src="img/maarten-deckers-T5nXYXCf50I-unsplash-1500x750.jpg"
            alt="Architecture"
          /></a
        >
        <p>
          <a href="/">Donec sit amet</a><br />
          <small
            >Class aptent taciti sociosqu ad litora torquent per conubia nostra</small
          >
        </p>
        <a href="/" aria-label="Example"
          ><img
            src="img/daniel-von-appen-tb4heMa-ZRo-unsplash-1500-750.jpg"
            alt="Architecture"
          /></a
        >
        <p>
          <a href="/">Suspendisse potenti</a><br />
          <small>Proin non condimentum tortor. Donec in feugiat sapien.</small>
        </p>
        <a href="/" aria-label="Example"
          ><img
            src="img/matthew-hamilton-Ru3Ap8TNcsk-unsplash-1500-750.jpg"
            alt="Architecture"
          /></a
        >
        <p>
          <a href="/">Nullam lobortis placerat aliquam</a><br />
          <small
            >Maecenas vitae nibh blandit dolor commodo egestas vel eget neque.
            Praesent semper justo orci, vel imperdiet mi auctor in.</small
          >
        </p>
      </aside>
    </div>
  </main>
  <!-- ./ Main -->

  <!-- Subscribe -->
  <section aria-label="Subscribe example">
    <div class="container">
      <article>
        <hgroup>
          <h2>Subscribe</h2>
          <h3>Litora torquent per conubia nostra</h3>
        </hgroup>
        <form class="grid">
          <input
            type="text"
            id="firstname"
            name="firstname"
            placeholder="First name"
            aria-label="First name"
            required
          />
          <input
            type="email"
            id="email"
            name="email"
            placeholder="Email address"
            aria-label="Email address"
            required
          />
          <button type="submit">Subscribe</button>
        </form>
      </article>
    </div>
  </section>
  <!-- ./ Subscribe -->

  <Footer />
</body>

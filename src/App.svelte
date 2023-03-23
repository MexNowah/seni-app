<script lang="ts">

  import seniLogo from './assets/images/logo-seni.png'
  import seniBackground from './assets/images/login-background.png'
  import Counter from './lib/Counter.svelte'

  let credentials = {
    email: "",
    password: "",
  };

  function handleOnSubmit() {
		console.log(credentials, 'credentials')
	}

</script>

<main>
  <div class="z-40 relative container mx-auto">
    <a href="https://svelte.dev" target="_blank" rel="noreferrer">
      <img src={seniLogo} class="logo mx-auto svelte" alt="Svelte Logo" />
    </a>

    <div class="">

      <form name="login-form" on:submit={handleOnSubmit}>
        <label class="block">
          <span class="block text-sm font-medium text-gray-600	 text-left">Correo Electrónico</span>
          <!-- Using form state modifiers, the classes can be identical for every input -->
          <input type="text" bind:value={credentials.email} class="mt-1 block w-full text-gray-600	 px-3 py-2 bg-white border border-slate-300 rounded-md text-sm shadow-sm placeholder-slate-400
            focus:outline-none focus:border-sky-500 focus:ring-1 focus:ring-sky-500
            disabled:bg-slate-50 disabled:text-slate-500 disabled:border-slate-200 disabled:shadow-none
            invalid:border-pink-500 invalid:text-pink-600
            focus:invalid:border-pink-500 focus:invalid:ring-pink-500
          "/>
        </label>

        <label class="block mt-2">
          <span class="block text-sm font-medium text-gray-600 text-left">Contraseña</span>
          <!-- Using form state modifiers, the classes can be identical for every input -->
          <input type="password" bind:value={credentials.password} class="mt-1 block w-full text-gray-600	 px-3 py-2 bg-white border border-slate-300 rounded-md text-sm shadow-sm placeholder-slate-400
            focus:outline-none focus:border-sky-500 focus:ring-1 focus:ring-sky-500
            disabled:bg-slate-50 disabled:text-slate-500 disabled:border-slate-200 disabled:shadow-none
            invalid:border-pink-500 invalid:text-pink-600
            focus:invalid:border-pink-500 focus:invalid:ring-pink-500
          "/>
        </label>

        <button on:click={handleOnSubmit} class="mt-4 rounded-md bg-sky-500 text-white">Inicia Sesión</button>

      </form>
    
    </div >
  </div>

  <div class="z-10 background">
    
  </div>
  
</main>

<style>
  .logo {
    height: 9em;
    width: 75vw;
    padding: 1.5em;
    will-change: filter;
    transition: filter 300ms;
    object-fit: contain;
  }
  .logo:hover {
    filter: drop-shadow(0 0 2em #646cffaa);
  }
  .logo.svelte:hover {
    filter: drop-shadow(0 0 2em #ff3e00aa);
  }
  .read-the-docs {
    color: #888;
  }

  .background {
    position: absolute;
    height: 100vh;
    width: 100%;
    top:0;
    left: 0;
    background-image: url('./assets/images/login-background.png');
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
  }
  .background-image{

  }
</style>

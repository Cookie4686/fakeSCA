<script>
  import Media from "../components/media.svelte";
</script>

<svelte:head>
  <title>Home</title>
</svelte:head>

<main>
  <div class="logo flex justify-center">
    <img src="/src/public/SCAlogo2023.png" alt="SCA logo" draggable="false" class="select-none">
  </div>
  <div class="flex flex-wrap justify-center gap-4">
    <p class="trademark text-center text-[1.5rem]">
      <span class="font-bold">โรงเรียนสามมุกคริสเตียนวิทยา</span>
      <br/>
      <span>Sammuk Christian Academy</span>
    </p>
    <div class="inline-flex w-full justify-center gap-8">
      <button class="btn btn-1"><a href="/" target="_blank">Photo Albums | ภาพกิจกรรม</a></button>
      <button class="btn btn-2"><a href="/">Home Page | เข้าสู่เว็บไซต์</a></button>
    </div>
    <Media></Media>
  </div>
</main>


<style>
  main {
    min-height: 100vh;
    padding: 2.5% 2.5%;
    background: #1D2152 url(/src/public/bg.svg) no-repeat center bottom;
    background-size: cover;
    color: white;
  }
  main > div {
    padding: 1rem 0;
  }
  .logo {
    padding: 1.5rem 0 4rem 0;
  }
  .logo img {
    width: clamp(7.5rem,20%,12.5rem);
  }
  .btn {
    width: clamp(7.5rem,33%,15.5rem);
  }
  .btn a {
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
  }
  .btn-1 {
    color: white;
    border-color: white;
    background-color: transparent;
  }
  .btn-2 {
    color: var(--blue);
    border-color: var(--lightblue);
  }
  .btn-2:hover {
    background-color: var(--yellow);
  }

  /* Tablet */
  @media all and (min-width:500px) {
    main {
      padding: 5% 5%;
    }
    .trademark {
      font-size: 2.25rem;
    }

  }
  /* Desktop */
  @media all and (min-width:768px) {
    .trademark {
      font-size: 2.5rem;
    }
  }
</style>
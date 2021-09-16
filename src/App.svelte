<script lang="ts">
  import Tailwind from "./Tailwind.svelte";
  import Canvas from "./Canvas.svelte";

  
  
  </script>
<style global lang="postcss">
      @tailwind base;
      @tailwind components;
      @tailwind utilities;
</style>
<svelte:head>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/animejs/3.2.1/anime.min.js"></script>
</svelte:head>
<Tailwind />
<Canvas />

<!--
<main class="container mx-auto">
  <div class="bg-gray-200 px-4 py-2 rounded">Hello Tailwind!</div>
  <Button>A Button</Button>
  <Logo name={"A Logo"} />
</main>
-->

<canvas id="c" class="fixed"></canvas>
<main id="main" class="main relative h-screen flex-grow container mx-auto justify-center max-w-screen-lg space-y-10">
  <section id="top" class="items-center w-full bg-white bg-opacity-50 shadow-xl m-0">
    <!-- <div class="welcome "> -->
      <h1 id="welcome" class="mx-auto flex-grow p-10 m-0 bg-no-repeat bg-white pl-40 font-bold">Welcome to DoctorEw's Lab</h1>
      <picture>
        <source srcset="https://www.doctorew.com/shuttlebay/doctor-doctor-doctor.webp" type="image/webp" />
      </picture>
    <!-- </div> -->
  </section>
  <section id="chat" class="items-center w-full bg-white bg-opacity-50 shadow-xl m-0">
    <h1 id="skippistan" class="mx-auto flex-grow p-10 m-0 bg-no-repeat bg-white pl-40 font-bold">Chat with Skippy the Magnificent!:</h1>
      <form class="mx-auto flex p-6">
        <div class="input text">
          <label for="chat_box" class="active">
            
          </label>
          <textarea id="chat_box" class="mx-auto flex p-6 bg-white rounded-lg shadow-xl bg-no-repeat pl-40 font-bold" name="chat_box" placeholder="Chat with Skippy the Magnificent!" required=""></textarea>
        </div>
      </form>
      <div id="chat_log"></div>
  </section>
</main>
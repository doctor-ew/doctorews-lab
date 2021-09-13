<script lang="ts">
  import Tailwind from "./Tailwind.svelte";

  const draw_drew_img = () => {
  const image = new Image();
  image.src = "https://www.doctorew.com/shuttlebay/doctor-doctor-doctor.png";
  image.onload = () => {
    const picture = document.querySelector("picture");
    const canvas = document.createElement("canvas");
    canvas.width = image.width;
    canvas.height = image.height;

    const context = canvas.getContext("2d");
    context.drawImage(image, 0, 0);
    picture.appendChild(canvas);
  };
};
  
</script>
<style global lang="postcss">
      @tailwind base;
      @tailwind components;
      @tailwind utilities;
</style>
<Tailwind />

<!--
<main class="container mx-auto">
  <div class="bg-gray-200 px-4 py-2 rounded">Hello Tailwind!</div>
  <Button>A Button</Button>
  <Logo name={"A Logo"} />
</main>
-->

<canvas id="c" class="h-screen h-width absolute"></canvas>
<main class="container mx-auto relative">
  <section id="top" class="items-center flex justify-center">
    <div class="welcome">
      <picture>
        <source srcset="https://www.doctorew.com/shuttlebay/doctor-doctor-doctor.webp" type="image/webp" />
      </picture>
      <h1 class="max-w-sm mx-auto flex p-6 bg-white rounded-lg shadow-xl">Welcome to DoctorEw's Lab</h1>
    </div>
  </section>
</main>
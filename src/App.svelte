<script>
  import { onMount } from "svelte";
  let home_animate = false;
  onMount(() => {
    setTimeout(() => {
      home_animate = true;
    }, 500);
  });
</script>

<main>
  <div id="box" class:animate={home_animate}></div>
</main>

<style>
  main {
    background-image: url("./assets/home-cube.svg");
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;
    width: 100vw;
    height: 100vh;
  }

  @keyframes box_open {
    from {
      width: 0px;
      height: 0px;
    }
    to {
      width: min(1280px, calc(100vw - 70px));
      height: min(800px, calc(100vh - 70px));
    }
  }

  #box {
    color: white;
    overflow: auto;
    position: fixed;
    top: 50%;
    left: 50%;
    width: 0px;
    height: 0px;
    transform: translate(-50%, -50%);
    backdrop-filter: blur(30px);
    background-color: rgba(127, 127, 127, 0.2);
    box-shadow: 0px 0px 0px 1px rgba(255, 255, 255, 0.15);
    border-radius: 16px;
    border: 10px solid transparent;
  }
  #box.animate {
    animation: box_open 1.25s cubic-bezier(0.65, 0, 0.35, 1) forwards;
  }
</style>

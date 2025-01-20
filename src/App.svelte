<script>
</script>

<main>
  <div id=box></div>
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

  #box {
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    backdrop-filter: blur(5px);
    padding: 20px;
    min-width: 125px;
    max-width: calc(100vw - 70px);
    min-height: 7px;
    max-height: calc(100vh - 70px);
    transition: 0.3s width height ease-out;
    background-color: rgba(127, 127, 127, 0.1);
    box-shadow: 3px 3px 5px 0px rgba(127, 127, 127, 0.15), -2 -2 4px 0px rgba(127, 127, 127, 0.1), inset 2px 2px 5px 0px rgba(255, 255, 255, 0.1);
    border-radius: 16px;
  }
</style>

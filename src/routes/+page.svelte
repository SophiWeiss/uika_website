<div class="whole-main-page">
  <div class="navigation-bar">
    <h1>Welcome to Uika Website</h1>
  </div>
  <div class="main-boxes">
    <div class="box1 box"></div>
    <div class="box2 box"></div>
    <div class="box3 box"></div>
    <div class="box4 box"></div>
    <div class="box5 box"></div>
    <div class="box6 box"></div>
  </div>
</div>

<style>
  .main-boxes {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: repeat(2, 1fr);
    height: 100vh;
    background-color: #fff2fb;
    gap: 20px;
    position: relative;
    padding: 20px;
  }
  :global(body) {
    background-color: #fff2fb;
  }
  :global(h1) {
    color: #3c3666;
    text-align: center;
    vertical-align: center;
    margin-top: 50px;
    margin-bottom: 50px;
  }
  .box {
    border-radius: 20px;
    padding: 20px;
    background-color: #817ca9;
    position: relative;
    overflow: hidden;
  }
  .box::after {
    content: 'Coming soon • Coming soon • Coming soon	• Coming soon	• Coming soon	• Coming soon	• Coming soon	• Coming soon	• Coming soon	• Coming soon'; /* Текст повторяется, чтобы заполнить полосу */
    display: block;
    position: absolute;
    top: 80%;
    left: 0;
    width: 200%;
    transform: translate(-5%, -5%) rotate(-30deg);
    transform-origin: 0 0;
    background-color: #ebbb5d;
    color: #ffffff;
    text-align: center;
    padding: 5px 0;
    font-weight: bold;
    overflow: hidden;
    white-space: nowrap;
    pointer-events: none;
  }
</style>

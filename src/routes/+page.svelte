<div class="whole-main-page">
  <div class="navigation-bar">
    <h1>Welcome to Uika Website</h1>
  </div>
  <div class="main-boxes">
    <div class="box1 box">One</div>
    <div class="box2 box">Two</div>
    <div class="box3 box">Three</div>
    <div class="box4 box">Four</div>
    <div class="box5 box">Five</div>
    <div class="box6 box">Six</div>
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
  }
</style>

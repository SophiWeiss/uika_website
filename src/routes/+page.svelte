<div class="whole-main-page">
  <div class="navigation-bar">
    <h1>Welcome to Uika Website</h1>
  </div>
  <div class="main-boxes">
    <div class="box1">One</div>
    <div class="box2">Two</div>
    <div class="box3">Three</div>
    <div class="box4">Four</div>
    <div class="box5">Five</div>
    <div class="box6">Six</div>
  </div>
</div>

<style>
  .main-boxes {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-auto-rows: 100px;
  }

  .box1 {
    grid-column-start: 1;
    grid-column-end: 4;
    grid-row-start: 1;
    grid-row-end: 3;
  }

  .box2 {
    grid-column-start: 1;
    grid-row-start: 3;
    grid-row-end: 5;
  }
</style>

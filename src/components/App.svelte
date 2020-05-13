<script>
  let dateNow = new Date().getTime();
  let dateEnd = new Date('2020-07-14').getTime();
  let diff =  dateEnd - dateNow;
  let date = Math.round(diff/(1000*60*60*24));
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Pacifico&display=swap');
  :global(*) {
    box-sizing: border-box
  }
  :global(body, div) {
    font-family: 'Pacifico', cursive;
    margin: 0;
    padding: 0;
  }
  #myVideo {
    position: fixed;
    right: 0;
    bottom: 0;
    min-width: 100%;
    min-height: 100%;
  }
  .App {
    position: absolute;
    bottom: 0;
    top:0;
    color: #f1f1f1;
    width: 100%;
    background: rgba(24,96,179, 0.6)
  }
  .App-container {
    display: grid;
    grid-template-columns: minmax(auto,1280px);
    justify-content: center;
    align-items: center;
  }
  .App-content {
    display: flex;
    justify-content: space-between;
    align-items: center;
    position: relative;
  }
  .App img {
    width: 80%;
    height: auto;
  }

  .App-title {
    padding: 1em;
  }

  h1 {
    color: #f8cf2d;
    font-size: 70px;
    margin: 0;
    padding: 0;
    letter-spacing: 2px;
    text-shadow: 6px 6px 0px rgba(0,0,0,0.2)
  }
  p {
    font-size: 40px;
    margin: 0;
    padding: 0;
    letter-spacing: 1.2px;
    text-shadow: 3px 3px 0px rgba(0,0,0,0.1);
  }
  figure {
    margin: 0;
    padding:0;
    text-align: right;
  }
</style>

<video autoplay muted loop id="myVideo">
  <source src="https://arepa.s3.amazonaws.com/baby-bg.mp4" type="video/mp4">
</video>

<div class="App">
  <div class="App-container">
    <div class="App-content">
      <div class="App-title">
        <h1>Oscar Barajas Jr.</h1>
        <p>Dias estimados para nacer: {date}</p>
      </div>
      <div class="App-image">
        <figure>
          <img src="https://arepa.s3.amazonaws.com/bgbebeloper.png" alt="Oscar Barajas">
        </figure>
      </div>
    </div>
  </div>
</div>
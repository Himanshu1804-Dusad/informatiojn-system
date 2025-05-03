# informatiojn-system
1. Develop a web-based information system using basic technologies such as mark-up languages, stylesheets, JavaScript, PHP script, and databases
<!-- Index.html -->

html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Personal Website</title>
  <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css">
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      display: flex;
    }
    /* Vertical Sidebar */
    .sidebar {
      width: 220px;
      background-color: #222;
      color: #fff;
      height: 100vh;
      padding: 20px;
      box-sizing: border-box;
      position: fixed;
    }
    .sidebar h2 {
      font-size: 20px;
      border-bottom: 1px solid #fff;
      padding-bottom: 5px;
    }
    .sidebar a {
      color: #fff;
      display: block;
      margin: 10px 0;
      text-decoration: none;
    }
    .sidebar img {
      width: 100%;
      max-width: 180px;
      margin-top: 10px;
      border-radius: 5px;
    }
    .main-content {
      margin-left: 240px;
      padding: 20px;
      flex: 1;
    }
    header {
      background-color: #f0f0f0;
      padding: 20px;
      text-align: center;
    }
    article img {
      max-width: 150px;
      height: auto;
      border-radius: 10px;
    }
    footer {
      background-color: #f0f0f0;
      padding: 20px;
      text-align: center;
      margin-top: 40px;
    }
    table {
      border-collapse: collapse;
      width: 100%;
      margin-top: 20px;
    }
    table, th, td {
      border: 1px solid black;
      padding: 8px;
      text-align: center;
    }
    hr {
      border: none;
      border-top: 2px solid #ccc;
      margin: 20px 0;
    }
    .hobby-card {
      margin-bottom: 20px;
    }
    .hobby-image {
      width: 100%;
      height: 150px;
      border-radius: 10px;
      margin-bottom: 10px;
    }
    .music-table {
      border-collapse: collapse;
      width: 100%;
    }
    .music-table th, .music-table td {
      border: 1px solid black;
      padding: 8px;
      text-align: left;
    }
  </style>
</head>
<body>
  <div class="sidebar">
    <h2>News Feed</h2>
    <p>• Exam form due Friday</p>
    <p>• Club meeting on Saturday</p>
    <h2>Links</h2>
    <a href="https://www.wikipedia.org" target="_blank">Wikipedia</a>
    <a href="https://www.w3schools.com" target="_blank">W3Schools</a>
    <a href="https://www.python.org" target="_blank">
      Python.org <br>
      <img src="https://www.python.org/static/community_logos/python-logo.png" alt="Python Logo">
    </a>
    <a href="https://www.stackoverflow.com" target="_blank">
      StackOverflow <br>
      <img src="https://cdn.sstatic.net/Sites/stackoverflow/company/img/logos/so/so-icon.png" alt="Stack Overflow Logo">
    </a>
  </div>
  <div class="main-content">
    <header>
      <img src="https://picsum.photos/200/300" alt="Your Logo" title="Your Logo">
    </header>
    <nav>
      <ul>
        <li><a href="my-study-subject.html">My Study Subject</a></li>
        <li><a href="my-hobbies.html">My Hobbies</a></li>
        <li><a href="my-music.html">My Music</a></li>
        <li><a href="my-house.php">My House</a></li>
      </ul>
    </nav>
    <article>
      <h1 id="about-me">About Me</h1>
      <img src="https://picsum.photos/200/300" alt="My Photo">
      <p><b>Hello!</b> My name is <i>John Doe</i>. I am a passionate computer science student at XYZ University, currently in my second year. I enjoy building creative <u>web applications</u> and working on innovative solutions that combine technology and real-world impact.</p>
      <hr>
      <p>I’ve always been curious about how things work. From disassembling toys to understanding software systems, my <b>interest in technology</b> has grown over time. I’m especially interested in <i>AI, cloud computing, and cybersecurity</i>. <u>Learning and evolving</u> in this dynamic field keeps me motivated every day.</p>
      <hr>
      <p>In my free time, I engage in various activities such as blogging, video editing, and experimenting with new programming languages. I believe in consistent growth and <b><i><u>lifelong learning</u></i></b>. My goal is to become a cloud data engineer and work on large-scale impactful systems.</p>
      <h2>My Hobbies</h2>
      <div class="row">
        <div class="col-md-4">
          <div class="card hobby-card">
            <img class="hobby-image" src="https://picsum.photos/200/300" alt="Reading">
            <div class="card-body">
              <h5 class="card-title">Reading</h5>
              <p class="card-text">I enjoy reading books in my free time.</p>
              <button type="button" class="btn btn-primary" data-toggle="modal" data-target="#readingModal">Learn More</button>
              <audio controls>
                <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mp3">
              </audio>
            </div>
          </div>
        </div>
        <div class="col-md-4">
          <div class="card hobby-card">
            <img class="hobby-image" src="https://picsum.photos/200/301" alt="Hiking">
            <div class="card-body">
              <h5 class="card-title">Hiking</h5>
              <p class="card-text">I love hiking and exploring new trails.</p>
              <button type="button" class="btn btn-primary" data-toggle="modal" data-target="#hikingModal">Learn More</button>
              <audio controls>
                <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-2.mp3" type="audio/mp3">
              </audio>
            </div>
          </div>
        </div>
        <div class="col-md-4">
          <div class="card hobby-card">
            <img class="hobby-image" src="https://picsum.photos/200/302" alt="Gaming">
            <div class="card-body">
              <h5 class="card-title">Gaming</h5>
              <p class="card-text">I'm an avid gamer and enjoy playing various games.</p>
              <button type="button" class="btn btn-primary" data-toggle="modal" data-target="#gamingModal">Learn More</button>
              <audio controls>
                <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-3.mp3" type="audio/mp3">
              </audio>
            </div>
          </div>
        </div>
      </div>
      <div class="row">
        <div class="col-md-4">
          <div class="card hobby-card">
            <img class="hobby-image" src="https://picsum.photos/200/303" alt="Cooking">
            <div class="card-body">
              <h5 class="card-title">Cooking</h5>
              <p class="card-text">I enjoy cooking and trying new recipes.</p>
              <button type="button" class="btn btn-primary" data-toggle="modal" data-target="#cookingModal">Learn More</button>
              <audio controls>
                <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-4.mp3" type="audio/mp3">
              </audio>
            </div>
          </div>
        </div>
        <div class="col-md-4">
          <div class="card hobby-card">
            <img class="hobby-image" src="https://picsum.photos/200/304" alt="Traveling">
            <div class="card-body">
              <h5 class="card-title">Traveling</h5>
              <p class="card-text">I love traveling and exploring new places.</p>
              <button type="button" class="btn btn-primary" data-toggle="modal" data-target="#travelingModal">Learn More</button>
              <audio controls>
                <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-5.mp3" type="audio/mp3">
              </audio>
            </div>
          </div>
        </div>
      </div>
      <h1 id="my-music">My Music</h1>
      <table class="music-table">
        <tr>
          <th>Track Title</th>
          <th>Performer</th>
          <th>Audio/Video Track</th>
        </tr>
        <tr>
          <td>Happy</td>
          <td><a href="https://www.pharrellwilliams.com" target="_blank">Pharrell Williams</a></td>
          <td><audio controls><source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mp3">Your browser does not support the audio element.</audio></td>
        </tr>
        <tr>
          <td>Uptown Funk</td>
          <td><a href="https://www.brunomars.com" target="_blank">Bruno Mars</a></td>
          <td><video width="200" controls><source src="https://www.w3schools.com/tags/movie.mp4" type="video/mp4">Your browser does not support the video element.</video></td>
        </tr>
        <tr>
          <td>Crazy</td>
          <td><a href="https://www.gnarlsbarkley.com" target="_blank">Gnarls Barkley</a></td>
          <td><audio controls><source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-2.mp3" type="audio/mp3">Your browser does not support the audio element.</audio></td>
        </tr>
      </table>
    </article>
    <footer>
      <p>Contact Me: <a href="mailto:example@example.com">example@example.com</a> | <a href="tel:1234567890">1234567890</a> | <a href="https://www.facebook.com" target="_blank">Facebook</a></p>
      <p>Copyright 2024</p>
      <p>Site Created On: <strong>May 3, 2025</strong></p>
    </footer>
  </div>
  <!-- Modals -->
  <div class="modal fade" id="readingModal" tabindex="-1" role="dialog" aria-labelledby="readingModalLabel" aria-hidden="true">
    <div class="modal-dialog" role="document">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title" id="readingModalLabel">Reading</h5>
          <button type="button" class="close" data-dismiss="modal" aria-label="Close">
            <span aria-hidden="true">&times;</span>
          </button>
        </div>
        <div class="modal-body">
          <div id="readingCarousel" class="carousel slide" data-ride="carousel">
            <div class="carousel-inner">
              <div class="carousel-item active">
                <img class="d-block w-100" src="https://picsum.photos/200/300" alt="First slide">
              </div>
              <div class="carousel-item">
                <img class="d-block w-100" src="https://picsum.photos/200/301" alt="Second slide">
              </div>
              <div class="carousel-item">
                <img class="d-block w-100" src="https://picsum.photos/200/302" alt="Third slide">
              </div>
            </div>
            <a class="carousel-control-prev" href="#readingCarousel" role="button" data-slide="prev">
              <span class="carousel-control-prev-icon" aria-hidden="true"></span>
              <span class="sr-only">Previous</span>
            </a>
            <a class="carousel-control-next" href="#readingCarousel" role="button" data-slide="next">
              <span class="carousel-control-next-icon" aria-hidden="true"></span>
              <span class="sr-only">Next</span>
            </a>
          </div>
          <audio controls>
            <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mp3">
          </audio>
        </div>
        <div class="modal-footer">
          <button type="button" class="btn btn-secondary" data-dismiss="modal">Close</button>
        </div>
      </div>
    </div>
  </div>
  <div class="modal fade" id="hikingModal" tabindex="-1" role="dialog" aria-labelledby="hikingModalLabel" aria-hidden="true">
    <div class="modal-dialog" role="document">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title" id="hikingModalLabel">Hiking</h5>
          <button type="button" class="close" data-dismiss="modal" aria-label="Close">
            <span aria-hidden="true">&times;</span>
          </button>
        </div>
        <div class="modal-body">
          <div id="hikingCarousel" class="carousel slide" data-ride="carousel">
            <div class="carousel-inner">
              <div class="carousel-item active">
                <img class="d-block w-100" src="https://picsum.photos/200/300" alt="First slide">
              </div>
              <div class="carousel-item">
                <img class="d-block w-100" src="https://picsum.photos/200/301" alt="Second slide">
              </div>
              <div class="carousel-item">
                <img class="d-block w-100" src="https://picsum.photos/200/302" alt="Third slide">
              </div>
            </div>
            <a class="carousel-control-prev" href="#hikingCarousel" role="button" data-slide="prev">
              <span class="carousel-control-prev-icon" aria-hidden="true"></span>
              <span class="sr-only">Previous</span>
            </a>
            <a class="carousel-control-next" href="#hikingCarousel" role="button" data-slide="next">
              <span class="carousel-control-next-icon" aria-hidden="true"></span>
              <span class="sr-only">Next</span>
            </a>
          </div>
          <audio controls>
            <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-2.mp3" type="audio/mp3">
          </audio>
        </div>
        <div class="modal-footer">
          <button type="button" class="btn btn-secondary" data-dismiss="modal">Close</button>
        </div>
      </div>
    </div>
  </div>
  <div class="modal fade" id="gamingModal" tabindex="-1" role="dialog" aria-labelledby="gamingModalLabel" aria-hidden="true">
    <div class="modal-dialog" role="document">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title" id="gamingModalLabel">Gaming</h5>
          <button type="button" class="close" data-dismiss="modal" aria-label="Close">
            <span aria-hidden="true">&times;</span>
          </button>
        </div>
        <div class="modal-body">
          <div id="gamingCarousel" class="carousel slide" data-ride="carousel">
            <div class="carousel-inner">
              <div class="carousel-item active">
                <img class="d-block w-100" src="https://picsum.photos/200/300" alt="First slide">
              </div>
              <div class="carousel-item">
                <img class="d-block w-100" src="https://picsum.photos/200/301" alt="Second slide">
              </div>
              <div class="carousel-item">
                <img class="d-block w-100" src="https://picsum.photos/200/302" alt="Third slide">
              </div>
            </div>
            <a class="carousel-control-prev" href="#gamingCarousel" role="button" data-slide="prev">
              <span class="carousel-control-prev-icon" aria-hidden="true"></span>
              <span class="sr-only">Previous</span>
            </a>
            <a class="carousel-control-next" href="#gamingCarousel" role="button" data-slide="next">
              <span class="carousel-control-next-icon" aria-hidden="true"></span>
              <span class="sr-only">Next</span>
            </a>
          </div>
          <audio controls>
            <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-3.mp3" type="audio/mp3">
          </audio>
        </div>
        <div class="modal-footer">
          <button type="button" class="btn btn-secondary" data-dismiss="modal">Close</button>
        </div>
      </div>
    </div>
  </div>
  <?php
    $houseInfo = [
      'Number of Bedrooms' => 3,
      'Number of Bathrooms' => 2,
      'Street Address' => '123 Main St',
      'City' => 'New York',
      'State' => 'NY',
      'Zip' => '10001'
    ];

    echo '<h1>My House</h1>';
    echo '<table class="table table-striped">';
    echo '<tr><th>Category</th><th>Information

# Native-app
//Movies app
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Logo Splash Screen</title>
<style>
body {
  margin: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background-color: #f0f0f0; /* Background color */
}

.logo-container {
  text-align: center;
}

.logo {
  width: 200px; /* Adjust logo size as needed */
  height: auto;
}
</style>
</head>
<body>

<div class="logo-container">
  <img class="logo" src="your_logo.png" alt="Your Logo"> 
</div>

<script>
  setTimeout(function() {
    window.location.href = "index.html"; // Replace with the URL of your main page
  }, 3000); // 3000 milliseconds = 3 seconds
</script>

</body>
</html>

<!DOCTYPE html>
<html>
<head>
<title>Movie List</title>
<style>
  body {
    font-family: sans-serif;
    margin: 0;
  }

  .container {
    max-width: 960px;
    margin: 0 auto;
    padding: 20px;
  }

  .search-bar {
    margin-bottom: 20px;
  }

  .search-input {
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 5px;
    width: 100%;
  }

  .movie-list {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    grid-gap: 20px;
  }

  .movie-card {
    border: 1px solid #ccc;
    border-radius: 5px;
    padding: 10px;
    text-align: center;
  }

  .movie-card img {
    width: 100%;
    height: 200px;
    object-fit: cover;
    border-radius: 5px;
  }

  .movie-title {
    margin-top: 10px;
    font-weight: bold;
  }

  .movie-summary {
    margin-top: 5px;
    overflow: hidden;
    text-overflow: ellipsis;
    display: -webkit-box;
    -webkit-line-clamp: 2; 
    -webkit-box-orient: vertical; 
  }
</style>
</head>
<body>

  <div class="container">
    <div class="search-bar">
      <input type="text" class="search-input" placeholder="Search Movies">
    </div>

    <div class="movie-list">
      <div class="movie-card">
        <img src="movie1.jpg" alt="Movie 1">
        <h3 class="movie-title">Movie 1 Title</h3>
        <p class="movie-summary">This is a short summary of Movie 1. This is a short summary of Movie 1.</p>
        <a href="details.html">View Details</a>
      </div>
      

      <div class="movie-card">
        <img src="movie2.jpg" alt="Movie 2">
        <h3 class="movie-title">Movie 2 Title</h3>
        <p class="movie-summary">This is a short summary of Movie 2. This is a short summary of Movie 2.</p>
        <a href="details.html">View Details</a>
      </div>
    <div class="movie-list">
      <div class="movie-card">
        <img src="movie3.jpg" alt="Movie 3">
        <h3 class="movie-title">Movie 1 Title</h3>
        <p class="movie-summary">This is a short summary of Movie 1. This is a short summary of Movie 1.</p>
        <a href="details.html">View Details</a>
      </div>


      </div> 

  </div>

</body>
</html>
<!DOCTYPE html>
<html>
<head>
<title>Movie List</title>
<style>
  body {
    font-family: sans-serif;
    margin: 0;
  }

  .container {
    max-width: 960px;
    margin: 0 auto;
    padding: 20px;
  }

  .search-bar {
    margin-bottom: 20px;
  }

  .search-input {
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 5px;
    width: 100%;
  }

  .movie-list {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    grid-gap: 20px;
  }

  .movie-card {
    border: 1px solid #ccc;
    border-radius: 5px;
    padding: 10px;
    text-align: center;
  }

  .movie-card img {
    width: 100%;
    height: 200px;
    object-fit: cover;
    border-radius: 5px;
  }

  .movie-title {
    margin-top: 10px;
    font-weight: bold;
  }

  .movie-summary {
    margin-top: 5px;
    overflow: hidden;
    text-overflow: ellipsis;
    display: -webkit-box;
    -webkit-line-clamp: 2; 
    -webkit-box-orient: vertical; 
  }
</style>
</head>
<body>

  <div class="container">
    <div class="search-bar">
      <input type="text" class="search-input" placeholder="Search Movies">
    </div>

    <div class="movie-list">
      <div class="movie-card">
        <img src="movie1.jpg" alt="Movie 1">
        <h3 class="movie-title">Movie 1 Title</h3>
        <p class="movie-summary">This is a short summary of Movie 1. This is a short summary of Movie 1.</p>
        <a href="details.html">View Details</a>
      </div>
      

      <div class="movie-card">
        <img src="movie2.jpg" alt="Movie 2">
        <h3 class="movie-title">Movie 2 Title</h3>
        <p class="movie-summary">This is a short summary of Movie 2. This is a short summary of Movie 2.</p>
        <a href="details.html">View Details</a>
      </div>
    <div class="movie-list">
      <div class="movie-card">
        <img src="movie3.jpg" alt="Movie 3">
        <h3 class="movie-title">Movie 1 Title</h3>
        <p class="movie-summary">This is a short summary of Movie 1. This is a short summary of Movie 1.</p>
        <a href="details.html">View Details</a>
      </div>


      </div> 

  </div>

</body>
</html>

<!DOCTYPE html>
<html>
<head>
<title>Movie Search</title>
<style>
  /* ... (CSS styles as in the previous example) ... */ 
</style>
</head>
<body>

  <div class="container">
    <div class="search-bar">
      <input type="text" id="searchInput" class="search-input" placeholder="Search Movies">
      <button onclick="searchMovies()">Search</button>
    </div>

    <div id="movieList" class="movie-list"></div> 

  </div>

  <script>
    async function searchMovies() {
      const searchTerm = document.getElementById('searchInput').value;
      const apiKey = 'YOUR_API_KEY'; // Replace with your actual API key
      const apiUrl = `https://api.example.com/search?query=${searchTerm}&api_key=${apiKey}`; 

      try {
        const response = await fetch(apiUrl);
        const data = await response.json();

        const movieList = document.getElementById('movieList');
        movieList.innerHTML = ''; 

        data.results.forEach(movie => {
          const movieCard = document.createElement('div');
          movieCard.classList.add('movie-card');

          const movieImage = document.createElement('img');
          movieImage.src = `https:Google. com//image.tmdb.org/t/p/w500/${movie.poster_path}`; // Example poster path
          movieImage.alt = movie.title;
          movieCard.appendChild(movieImage);

          const movieTitle = document.createElement('h3');
          movieTitle.classList.add('movie-title');
          movieTitle.textContent = movie.title;
          movieCard.appendChild(movieTitle);

          const movieSummary = document.createElement('p');
          movieSummary.classList.add('movie-summary');
          movieSummary.textContent = movie.overview;
          movieCard.appendChild(movieSummary);

          const viewDetailsLink = document.createElement('a');
          viewDetailsLink.href = `details.html?id=${movie.id}`; // Pass movie ID to details page
          viewDetailsLink.textContent = 'View Details';
          movieCard.appendChild(viewDetailsLink);

          movieList.appendChild(movieCard);
        });

      } catch (error) {
        console.error('Error fetching movies:', error);
        // Display an error message to the user
      }
    }
  </script>

</body>
</html>
<!DOCTYPE html>
<html>
<head>
<title>Splash Screen & Home Page</title>
<style>
  /* Splash Screen Styles */
  body {
    margin: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: #282c34; /* Dark background for splash screen */
  }

  .splash-screen {
    text-align: center;
    color: #fff;
  }

  /* Home Page Styles */
  .home-container {
    max-width: 960px;
    margin: 0 auto;
    padding: 20px;
  }

  .search-bar {
    margin-bottom: 20px;
  }

  .search-input {
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 5px;
    width: 100%;
  }

  .image-container {
    position: relative;
    overflow: hidden;
  }

  .image-container img {
    width: 100%;
    height: auto;
    transition: transform 0.5s ease-in-out; 
  }

  /* Animation for moving effect */
  .move-left {
    animation: moveLeft 10s infinite; 
  }

  @keyframes moveLeft {
    0% { transform: translateX(0); }
    100% { transform: translateX(-50%); } 
  }

</style>
</head>
<body>

  <div class="splash-screen" id="splashScreen">
    <h1>Welcome</h1>
    <p>Loading...</p>
  </div>

  <div class="home-container" id="homePage" style="display: none;"> 
    <div class="search-bar">
      <input type="text" class="search-input" placeholder="Search...">
    </div>

    <div class="image-container">
      <img src="image.jpg" alt="Image" class="move-left"> 
    </div>

  </div>

  <script>
    setTimeout(() => {
      const splashScreen = document.getElementById('splashScreen');
      splashScreen.style.display = 'none';

      const homePage = document.getElementById('homePage');
      homePage.style.display = 'block';
    }, 5000); // 5 seconds delay for splash screen
  </script>

</body>
</html>


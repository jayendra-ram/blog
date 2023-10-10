<script lang="ts">
	import { page } from '$app/stores';
  </script>
  
  <header class="header">
	<div class="header-content">
	  <a href="/">
		<h1 class:small={$page.url.pathname !== "/"}>jay's world</h1>
	  </a>
	  <p>
		<i>assorted ideas</i>
	  </p>
	</div>
	<div class="header-background"></div>
  </header>
  
  <main class="content">
	<slot />
  </main>
  
  <!-- <footer class="footer">
	<p>
	  &copy; <a href="https://twitter.com/jayendra_ram">jayendra ram</a>, {new Date().getFullYear()}
	</p>
  </footer> -->
  
  <style>
	.header {
	  display: flex;
	  flex-direction: column;
	  justify-content: center;
	  align-items: center;
	  position: relative;
	  z-index: 1;
	  padding: 2rem;
	  text-align: center;
	  color: white;
	  height: 20vh;
	}
  
	.header-content {
	  position: relative;
	  z-index: 2;
	}
  
	.header h1 {
	  font-size: 3rem;
	  margin: 0;
	  font-family: 'Montserrat', sans-serif;
	  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
	  color: #ffffff;
	}
  
	.header p {
	  font-size: 1.5rem;
	  margin: 0;
	  font-family: 'Montserrat', sans-serif;
	  text-shadow: 4px 4px 6px rgba(0, 0, 0, 0.5);
	  color: #fee1af;
	}
  
	.header-background {
	  position: absolute;
	  top: 0;
	  left: 0;
	  width: 100%;
	  height: 100%;
	  background-image: url("https://www.sriramanamaharshi.org/wp-content/uploads/2013/01/Arunachala_gallery-6.jpg");
	  background-size: cover;
	  background-position: center bottom 400px;
	  transform-origin: center bottom;
	  scale: 1.2;
	}
  
	.content {
	  padding: 2rem;
	  max-width: 75ch;
	  margin: 0 auto;
	  font-size: 1.2rem;
	  font-family: 'Montserrat', sans-serif;
	  line-height: 1.5;
	}
  
	.footer {
		bottom: 0;
		width: 100%;
		height: 6rem;
		font-size: 1.2rem;
		font-family: 'Montserrat', sans-serif;
	}
	.footer a {
	  color: #666;
	  font-weight: bold;
	}
  
  </style>
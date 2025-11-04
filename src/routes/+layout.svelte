<script>
	import { page } from '$app/stores';
	import '../app.css';
  </script>
  
  <nav>
	<div class="nav-container">
	  <div class="logo">My Blog</div>
	  <ul class="nav-links">
		<li class:active={$page.url.pathname === '/'}>
		  <a href="/">Home</a>
		</li>
		<li class:active={$page.url.pathname === '/about'}>
		  <a href="/about">About</a>
		</li>
		<li class:active={$page.url.pathname.startsWith('/blog')}>
		  <a href="/blog">Blog</a>
		</li>
	  </ul>
	</div>
  </nav>
  
  <main>
	<slot />
  </main>
  
  <footer>
	<p>© {new Date().getFullYear()} My Blog. All rights reserved.</p>
  </footer>
  
  <style>
	.nav-container {
	  display: flex;
	  justify-content: space-between;
	  align-items: center;
	  padding: 1rem 2rem;
	  background-color: #f8f9fa;
	}
	
	.logo {
	  font-size: 1.5rem;
	  font-weight: bold;
	}
	
	.nav-links {
	  display: flex;
	  list-style: none;
	  gap: 2rem;
	  margin: 0;
	  padding: 0;
	}
	
	.nav-links a {
	  text-decoration: none;
	  color: #333;
	  font-weight: 500;
	}
	
	.active a {
	  color: #ff3e00;
	}
	
	main {
	  max-width: 800px;
	  margin: 2rem auto;
	  padding: 0 1rem;
	  min-height: calc(100vh - 160px);
	}
	
	footer {
	  text-align: center;
	  padding: 1rem;
	  background-color: #f8f9fa;
	}
  </style>
  

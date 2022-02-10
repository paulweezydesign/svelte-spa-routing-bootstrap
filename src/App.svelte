<script>
	import Router, {location, link} from 'svelte-spa-router';
	import Home from './Home.svelte';
	import About from './About.svelte';
	import Contact from './Contact.svelte';
	import Blog from './Blog.svelte';
</script>

<nav>
	<a  href="/">Home</a>
	<a href="/#/about">About</a>
	<a href="/#/contact">Contact</a>
	<a href="/#/blog/colors">Colors</a>
</nav>

<Router routes={{
	'/': Home,
	'/about': About,
	'/contact': Contact,
	'/blog/:blogName': Blog
}} />

<hr>
/#{$location}
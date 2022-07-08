<!DOCTYPE html>
<html>
<head>
</head>
<body>
<h1>Laravel 9 With Vite</h1>
 
<h4>1: Install Laravel Project</h4>
<pre> 
	composer create-project laravel/laravel laravel-vite
</pre> 

<h4>2: Install Laravel UI</h4>
<pre> 
	composer require laravel/ui
</pre> 

<h4>3: Auth Scaffolding </h4>
<pre> 
	php artisan ui bootstrap
	php artisan ui bootstrap --auth
</pre> 

<h4>4: Change vite.config.js </h4>
<pre> 
	import { defineConfig } from 'vite';
	import laravel from 'laravel-vite-plugin';
	import path from 'path'

	export default defineConfig({
	    plugins: [
	        laravel([
	            'resources/js/app.js',
	        ]),
	    ],
	    resolve: {
	        alias: {
	            '~bootstrap': path.resolve(__dirname, 'node_modules/bootstrap'),
	        }
	    },
	});
</pre> 


<h4>5: Import Bootstrap SCSS in JS Folder</h4>
<pre> 
	Path : resources/js/app.js
	
	import './bootstrap';
	import '../sass/app.scss'
	import * as bootstrap from 'bootstrap'
</pre> 

<h4>6: Replace mix() with @vite Blade directive</h4>
<pre> 
	Path : resources\views\layouts\app.blade.php

	@vite(['resources/js/app.js'])  
</pre> 

<h4>7: Running Vite Command to build Asset File </h4>
<pre> 
	npm install && npm run dev
	npm run build 
</pre> 

<h4>8: Running </h4>
<pre> 
	http://127.0.0.1:8000  
</pre> 

<p>Enjoy coding ........ </p>

</body>
</html>

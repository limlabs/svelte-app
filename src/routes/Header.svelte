<script lang="ts">
	import { page } from '$app/stores';
	import logo from '$lib/images/svelte-logo.svg';
	import Icons from '$lib/components/ui/Icons.svelte';

	const currentPath = $derived($page.url.pathname);
</script>

<!-- Top Bar -->
<div class="top-bar">
    <div class="container">
        <div class="contact-info">
            <span class="inline-flex items-center gap-3 text-sm"><Icons type="phone" size={16} color="#2563eb" />(555) 123-4567</span>
            <span class="inline-flex items-center gap-3 text-sm ml-6"><Icons type="mail" size={16} color="#2563eb" />info@limo.com</span>
        </div>
    </div>
</div>

<header>
	<div class="container">
		<a href="/" class="logo">Limo</a>

	<nav class="main-nav">
		<ul>
			<li class="nav-item" aria-current={currentPath === '/' ? 'page' : undefined}>
				<a href="/">Home</a>
			</li>
			<li class="nav-item" aria-current={currentPath === '/about' ? 'page' : undefined}>
				<a href="/about">About</a>
			</li>
			<li class="nav-item" aria-current={currentPath === '/services' ? 'page' : undefined}>
				<a href="/services">Services</a>
			</li>
			<li class="nav-item" aria-current={currentPath === '/contact' ? 'page' : undefined}>
				<a href="/contact">Contact</a>
			</li>
		</ul>
	</nav>
	</div>
</header>

<style>
	.top-bar {
		background: #f0f9ff;
		border-bottom: 1px solid #e5e7eb;
		padding: 0.5rem 0;
		display: none;
	}

	@media (min-width: 768px) {
		.top-bar {
			display: block;
		}
	}

	.contact-info {
		display: flex;
		gap: 1rem;
		color: #4b5563;
		font-size: 0.875rem;
	}

    header {
        background: white;
        border-bottom: 1px solid #e5e7eb;
        position: sticky;
        top: 0;
        z-index: 50;
    }

    .container {
        display: flex;
        justify-content: space-between;
        align-items: center;
        height: 4rem;
        padding: 0 1rem;
    }

    .logo {
        font-size: 1.5rem;
        font-weight: bold;
        color: #2563eb;
        text-decoration: none;
    }

    .main-nav {
        display: none;
    }

    @media (min-width: 768px) {
        .main-nav {
            display: flex;
            align-items: center;
        }
    }

    .main-nav ul {
        display: flex;
        gap: 1.5rem;
        list-style: none;
        margin: 0;
        padding: 0;
    }

    .nav-item a {
        color: #4b5563;
        text-decoration: none;
        font-size: 0.875rem;
        transition: color 0.2s;
    }

    .nav-item a:hover {
        color: #2563eb;
    }

    .nav-item[aria-current='page'] a {
        color: #2563eb;
        font-weight: 500;
    }
</style>

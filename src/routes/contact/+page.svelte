<script lang="ts">
</script>

<svelte:head>
    <title>Contact Us - Limo</title>
    <meta name="description" content="Get in touch with our team" />
</svelte:head>

<div class="container">
    <h1>Contact Us</h1>
    <p>Have questions? We're here to help.</p>
    
    <div class="contact-info">
        <div class="info-item">
            <h2>Phone</h2>
            <p>(555) 123-4567</p>
        </div>
        <div class="info-item">
            <h2>Email</h2>
            <p>info@limo.com</p>
        </div>
    </div>
</div>

<style>
    .container {
        max-width: 1200px;
        margin: 0 auto;
        padding: 2rem 1rem;
    }

    h1 {
        font-size: 2.5rem;
        font-weight: bold;
        margin-bottom: 1rem;
    }

    p {
        color: #4b5563;
    }

    .contact-info {
        margin-top: 2rem;
    }

    .info-item {
        margin-bottom: 1.5rem;
    }

    .info-item h2 {
        font-size: 1.25rem;
        font-weight: 600;
        margin-bottom: 0.5rem;
    }
</style>

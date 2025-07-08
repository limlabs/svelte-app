<script lang="ts">
    import background from '$lib/images/background.jpg';
    import type { WhyChooseUsFeature } from '$lib/types';

    let isHovered = $state(false);
    let activeFeature = $state<number>(0);
    let activeQuestion = $state<number>(-1);

    const whyChooseUsFeatures: WhyChooseUsFeature[] = [
        {
            title: 'Process Automation',
            description: 'Automate repetitive tasks and workflows to save time and reduce errors.',
            metric: '85%',
            metricLabel: 'Time Saved'
        },
        {
            title: 'Data Analytics',
            description: 'Get actionable insights from your business data with advanced analytics.',
            metric: '2x',
            metricLabel: 'Faster Decisions'
        },
        {
            title: 'Cloud Integration',
            description: 'Seamlessly connect your existing tools and systems in the cloud.',
            metric: '99.9%',
            metricLabel: 'Uptime'
        }
    ];

    function onGetStartedClick() {
        // TODO: Implement get started flow
        console.log('Get Started clicked');
    }

    function onFeatureClick(index: number) {
        activeFeature = index;
    }
</script>

<svelte:head>
    <title>Home</title>
    <meta name="description" content="Modern business solutions" />
</svelte:head>

<section class="hero w-full">
    <div class="container">
        <div class="hero-content">
            <div>
                <div class="badge">Trusted by 500+ Companies</div>
                <h1>
                    Simplify Your <span class="highlight">Business Processes</span>
                </h1>
                <p>
                    Limo helps businesses streamline operations, reduce costs, and improve efficiency with our innovative solutions.
                </p>
                <div class="button-group">
                    <button class="primary" onclick={onGetStartedClick}>
                        Get Started
                        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="ml-2"><path d="M5 12h14"></path><path d="m12 5 7 7-7 7"></path></svg>
                    </button>
                    <button class="secondary">Learn More</button>
                </div>
            </div>
            <div class="hero-image">
                <img src={background} alt="Business dashboard" />
            </div>
        </div>
    </div>
</section>

<section class="features">
    <div class="container">
        <div class="section-header">
            <div class="badge">Our Offerings</div>
            <h2>Our Services</h2>
            <p>We offer a range of services to help your business thrive in today's competitive market.</p>
        </div>
        <div class="feature-grid">
            <div class="feature-card">
                <div class="icon-circle">
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="check-icon"><polyline points="20 6 9 17 4 12"></polyline></svg>
                </div>
                <h3>Business Consulting</h3>
                <p>Expert advice to optimize your business operations and increase profitability.</p>
                <ul class="feature-list">
                    <li>
                        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="check-icon-small"><polyline points="20 6 9 17 4 12"></polyline></svg>
                        <span>Strategic planning</span>
                    </li>
                    <li>
                        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="check-icon-small"><polyline points="20 6 9 17 4 12"></polyline></svg>
                        <span>Market analysis</span>
                    </li>
                    <li>
                        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="check-icon-small"><polyline points="20 6 9 17 4 12"></polyline></svg>
                        <span>Performance optimization</span>
                    </li>
                </ul>
                <button class="secondary full-width">Learn More</button>
            </div>

            <div class="feature-card">
                <div class="icon-circle">
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="check-icon"><polyline points="20 6 9 17 4 12"></polyline></svg>
                </div>
                <h3>Process Automation</h3>
                <p>Streamline your workflows with our cutting-edge automation solutions.</p>
                <ul class="feature-list">
                    <li>
                        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="check-icon-small"><polyline points="20 6 9 17 4 12"></polyline></svg>
                        <span>Workflow optimization</span>
                    </li>
                    <li>
                        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="check-icon-small"><polyline points="20 6 9 17 4 12"></polyline></svg>
                        <span>Custom automation tools</span>
                    </li>
                    <li>
                        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="check-icon-small"><polyline points="20 6 9 17 4 12"></polyline></svg>
                        <span>Integration services</span>
                    </li>
                </ul>
                <button class="secondary full-width">Learn More</button>
            </div>

            <div class="feature-card">
                <div class="icon-circle">
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="check-icon"><polyline points="20 6 9 17 4 12"></polyline></svg>
                </div>
                <h3>Digital Transformation</h3>
                <p>Transform your business with innovative digital solutions and strategies.</p>
                <ul class="feature-list">
                    <li>
                        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="check-icon-small"><polyline points="20 6 9 17 4 12"></polyline></svg>
                        <span>Technology assessment</span>
                    </li>
                    <li>
                        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="check-icon-small"><polyline points="20 6 9 17 4 12"></polyline></svg>
                        <span>Digital strategy development</span>
                    </li>
                    <li>
                        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="check-icon-small"><polyline points="20 6 9 17 4 12"></polyline></svg>
                        <span>Implementation support</span>
                    </li>
                </ul>
                <button class="secondary full-width">Learn More</button>
            </div>
        </div>
    </div>
</section>

<section class="faq">
    <div class="container">
        <div class="section-header">
            <div class="badge">FAQ</div>
            <h2>Frequently Asked Questions</h2>
            <p>Find answers to common questions about our services and solutions.</p>
        </div>
        <div class="faq-grid">
            <div class="faq-item">
                <button class="faq-question" onclick={() => activeQuestion = activeQuestion === 0 ? -1 : 0}>
                    <span>What services do you offer?</span>
                    <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class={activeQuestion === 0 ? 'rotate-180' : ''}><path d="m18 15-6-6-6 6"/></svg>
                </button>
                <div class="faq-answer" class:active={activeQuestion === 0}>
                    <p>We offer a comprehensive suite of business solutions including process automation, data analytics, cloud integration, and digital transformation services. Our solutions are designed to help businesses streamline operations and improve efficiency.</p>
                </div>
            </div>
            <div class="faq-item">
                <button class="faq-question" onclick={() => activeQuestion = activeQuestion === 1 ? -1 : 1}>
                    <span>How can I get started?</span>
                    <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class={activeQuestion === 1 ? 'rotate-180' : ''}><path d="m18 15-6-6-6 6"/></svg>
                </button>
                <div class="faq-answer" class:active={activeQuestion === 1}>
                    <p>Getting started is easy! Simply click the 'Get Started' button above or contact our team. We'll schedule a consultation to understand your needs and recommend the best solutions for your business.</p>
                </div>
            </div>
            <div class="faq-item">
                <button class="faq-question" onclick={() => activeQuestion = activeQuestion === 2 ? -1 : 2}>
                    <span>What makes Limo different?</span>
                    <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class={activeQuestion === 2 ? 'rotate-180' : ''}><path d="m18 15-6-6-6 6"/></svg>
                </button>
                <div class="faq-answer" class:active={activeQuestion === 2}>
                    <p>Our innovative approach combines cutting-edge technology with industry expertise. We focus on delivering measurable results, with proven success in reducing costs and improving efficiency for over 500 companies.</p>
                </div>
            </div>
        </div>
    </div>
</section>

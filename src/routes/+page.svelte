<script>
	import Button from "$lib/Button.svelte";
	import WorkCard from "$lib/WorkCard.svelte";
</script>

<div class="page-container">
	<div class="hero">
		<div class="hero-heading">
			<h1 class="h1-hero">I'm <strong>Brian</strong>.</h1>
			<h1 class="h1-hero">I speak <strong>person</strong> and <strong>code</strong>.</h1>
		</div>
		<div class="hero-p">
			<h6>I'm a User Experience Designer, a Web Developer, and a fellow person in this modern world.</h6>
			<h6>Our digital future is going to be anxious and exciting.</h6>
			<h6>I'd like to help keep it honest and lovely.</h6>
		</div>
		<div class="hero-button">
			<Button url="/about" text="More about me" />
		</div>
	</div>

	<div class="study-container">
		<h1>UX Design Work</h1>
		
		<!-- <WorkCard projectUrl="/projects/cob" tags="{['VoiceAssistanceTech', 'Design']}" title="Cobs of Bos"/>
		
		<div class="study">
			<h2>Long Form Case Study: <br/>Designing an Amazon Alexa Skill</h2>
			<figure>
				<img src="/images/Alexa_2.jpg" alt="An Alexa Echo device" style="max-width: 1000px;" />
				<figcaption></figcaption>
			</figure>
			<h3>Exploring New Voice Technology for an Old City</h3>
			<div class="study-summary">
				<p>Voice Assistants are still <strong>new</strong></p>
				<p>and <strong>a little buggy</strong>.</p>
				<p>We researched <strong>Amazon's Alexa</strong></p>
				<p>to give a new voice to <strong>the City of Boston</strong>.</p>
			</div>
			<Button url="/projects/cob" text="Learn more" />
		</div>
		<div class="study">
			<h2>Long Form Case Study: <br/>Designing an Amazon Alexa Skill</h2>
			<figure>
				<img src="/images/Alexa_2.jpg" alt="An Alexa Echo device" style="max-width: 1000px;" />
				<figcaption></figcaption>
			</figure>
			<h3>Exploring New Voice Technology for an Old City</h3>
			<div class="study-summary">
				<p>Voice Assistants are still <strong>new</strong></p>
				<p>and <strong>a little buggy</strong>.</p>
				<p>We researched <strong>Amazon's Alexa</strong></p>
				<p>to give a new voice to <strong>the City of Boston</strong>.</p>
			</div>
			<Button url="/projects/cob" text="Learn more" />
		</div> -->
		<div class="study">
			<h2>Long Form Case Study: <br/>Designing an Amazon Alexa Skill</h2>
			<figure>
				<img src="/images/Alexa_2.jpg" alt="An Alexa Echo device" style="max-width: 1000px;" />
				<figcaption></figcaption>
			</figure>
			<h3>Exploring New Voice Technology for an Old City</h3>
			<div class="study-summary">
				<p>Voice Assistants are still <strong>new</strong></p>
				<p>and <strong>a little buggy</strong>.</p>
				<p>We researched <strong>Amazon's Alexa</strong></p>
				<p>to give a new voice to <strong>the City of Boston</strong>.</p>
			</div>
			<Button url="/projects/cob" text="Learn more" />
		</div>
		
		<div class="study">
			<h2>Short Form Case Study: <br/>Designing "Search"</h2>
			<figure>
				<img src="/images/MindBody_2.png" alt="The MindBody logo" style="max-width: 1000px;" />
				<figcaption></figcaption>
			</figure>
			<h3>When Features and Branding Feel “Clunky”</h3>
			<div class="study-summary">
				<p>MindBody is an <strong>app for booking health and fitness classes</strong>...</p>
				<p>...But also haircuts and doctor's appointments.</p>
				<p>I worked in a team of 3 to <strong>identify the real needs of the users</strong>,</p>
				<p>and <strong>streamline the search and results</strong> pages.</p>
			</div>
			<Button url="/projects/mindbody" text="Learn more" />
		</div>

	</div>
</div>

<div class="page-container">
  <div class="quote-container">
    <h3>Brian Collura | Greater Boston, MA</h3>
    <p><a href="mailto:bjscollura@gmail.com" target="_blank">bjscollura@gmail.com</a></p>
    <blockquote>
      Yet none could better know than I, <br />
      how much of act at human hands <br />
      the sense of human will demands <br />
      by which we dare to live, or die.
    </blockquote>
    <p class="quote-signature">~ Alfred Lord Tennyson</p>
  </div>

  <div class="aboutme-container">
    <h3>Looking to learn more?</h3>
    <div class="subcontainer">
      <div class="p-container">
        <p>Thanks for taking the time! I’m Brian - I’m a User Experience Designer, a Web Developer, and an IT Engineer. Over the last 10 years, I’ve seen Full Stack development replace traditional web teams, I’ve watched BDD and DevOps automation commoditize the workflow, and I’ve helped implement frameworks and SaaS suites for my Applications teams as they came in and out of vogue. <strong>The pace of change has been rapid</strong>.</p>
        <p>But I’m also a Social Psychologist and a Customer Service Professional. While these burgeoning web technologies were made by brilliant and well-intentioned technologists, they don’t always allow coders to anticipate customer confusions and needs, testing <strong>user BEHAVIORS instead of user INTENTIONS</strong>. Meanwhile, these bigger-picture issues are more frequently being hunted down by code and AI, rather than human eyes.</p>
        <p>My skillset, my passion, and my primary aggravation are all the same - <strong>integrate customer service back into automated experiences.</strong> Someday, when we the consumers have the same control over our tech as we do our hammers and nails, I will be content with the world I’ve helped leave for the rest of us.</p>
      </div>
      <div class="img-container">
        <figure>
          <img src="/images/AboutMe_Pic.jpg" alt="Brian, looking as handsome as he can.">
          <figcaption></figcaption>
        </figure>
      </div>
    </div>
  </div>
</div>

<style>
	h3 {
		text-align: center;
	}
	.quote-container {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: space-between;
		max-width: 951px;
		padding: 2rem;
	}
	.quote-signature {
		align-self: flex-end;
	}
	blockquote {
		border-left: 2px solid #e4ebe4;
		padding: 3px 10px;
	}
	blockquote:before {
		content: '\201C';
		position: relative;
		top: 1rem;
		left: -50px;
		display: block;
		margin-bottom: -1.6rem;
		font-size: 3rem;
	}
  .aboutme-container {
    flex-direction: column;
    align-items: center;
    justify-content: space-between;
  }
  .subcontainer {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
  }
  .p-container {
	  display: flex;
	  flex-direction: column;
	  justify-content: space-between;
	  align-items: flex-start;
	  flex: 1;
	  max-width: 70ch;
	  margin: 0 25px;
	}
	.img-container {
		display: flex;
		align-items: center;
		justify-content: center;
		width: 38%;
	}
	@media only screen and (max-width: 999px) {
	 .subcontainer {
		 flex-direction: column;
	 }
	 .img-container {
		width: min(768px, 90%);
		margin-top: 2rem;
	 }
	}
</style>

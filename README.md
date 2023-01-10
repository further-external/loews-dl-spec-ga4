# loews-dl-spec-ga4

<h1 id="overview"><strong>Overview</strong></h1>
<p>This repository contains the necessary specifications to build an event driven data layer and install GTM on your web application.</p>
<h2 id="google-tag-manager-deployment">Google Tag Manager Deployment</h2>
<p>The embed code is a <strong>script</strong> tag that you put on your web pages to load and execute the logic you build in GTM, including logic to configure and deploy tags for analytics, 3rd parties, and other Google services.</p>
<p>To install GTM on your web application:</p>
<ol>
<li><p>In Google Tag Manager, click <strong>Workspace</strong></p></li>
<li><p>Near the top right corner of the window, find your container ID, formatted as "GTM-XXXXXX". Click the container ID to launch the Install Tag Manager modal.</p></li>
<li><p>Copy and paste the code snippets into your website as instructed in the Install Tag Manager box.</p></li>
</ol>
<div class="rich-media-item mediaSingleView-content-wrap image-center sc-ePZHVD kLKZTy sc-bEjcJn jjvZSm" data-layout="center" data-node-type="mediaSingle"><div class="sc-bGbJRg kUjBNf"><div class="new-file-experience-wrapper sc-eeMjtc czMCpw" data-testid="media-card-view"><div class="media-file-card-view sc-bhizqx jGLuht" data-testid="media-file-card-view" data-test-media-name="https://apollo-help-images.s3.amazonaws.com/gtm_install_instructions.png" data-test-status="complete"><img class="sc-drKuOJ eHwasM" draggable="false" src="https://apollo-help-images.s3.amazonaws.com/gtm_install_instructions.png" alt="" width="746" height="345" data-testid="media-image"></div></div></div></div>
<h3 id="implement-the-code-snippets-in-the-of-the-sample-html-page">Implement the Code Snippets in the of the Sample HTML Page</h3>
<p>Both code snippets should be implemented in the element of all HTML pages that will share the property. You might have one or several template files which control this globally across the site, making it a straightforward process.</p>
<p>Place the <code>&lt;script&gt;</code> code snippet in the <code>&lt;head&gt;</code> of your web page's HTML output, as close to the opening <code>&lt;head&gt;</code> tag as possible, but below any Data Layer object settings.</p>
<p>Place the <code>&lt;noscript&gt;</code> code snippet immediately after the <body> tag in your HTML output.</p>
<h2 id="data-layer">Data Layer</h2>
<p>Each file inside the events folder corresponds to a single use case or site event that needs to be implemented. These events are leveraged to trigger tracking rules in the tag management tool of choice and share data with the analytics reporting tool.</p>
<p>As the data layer is event-based, the order in which the events are fired is critical. In general, events should be pushed onto the data layer in the following sequence when a page load (virtual or otherwise) occurs:</p>
<p>Page Load Started &gt; <em>Other Page-level Events</em> &gt; Page Load Completed</p>
<p>If an Event is part of the page load sequence, it will be indicated in the corresponding event file.</p>
<p>Events that occur outside of the page load sequence should be pushed onto the data layer as they occur.</p>
<h2 id="questionscomments">Questions/Comments</h2>
<p>For any questions or comments, please contact&nbsp;anne.wilson@searchdiscovery.com.</p>
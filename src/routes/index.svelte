<h1>Identical Names Bug</h1>
<p>
	To reproduce this bug, simply navigate to the page below. This will navigate to a page located at
</p>
<pre>routes/atoms/button.svelte</pre>

<p>This page actually includes a single component, imported from</p>
<pre>$lib/components/atoms/Button.svelte</pre>

<a class="btn" href="/atoms/button">Go to "/atoms/button"</a>
<a class="btn" href="/info/installation">Go to "/info/installation"</a>

<style>
    a.btn {
        display: inline-block;
        border-radius: .25rem;
        padding: 1rem;
        background: orange;
        color: black;
        font-weight: 700;
    }

    pre {
        color: orange
    }
</style>
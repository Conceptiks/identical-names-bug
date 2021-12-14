<script>
	import { page } from '$app/stores';
</script>

<header>
	<pre>{$page.path}</pre>
</header>
<main>
	<slot />
</main>

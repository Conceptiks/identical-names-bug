<script>
    import { page } from '$app/stores';
    $: console.log($page)
</script>

{$page.path}
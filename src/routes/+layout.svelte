<script lang="ts">
	import Wrapper from '../components/wrapper.svelte';
	import Header from '../components/header.svelte';
	import Content from '../components/content.svelte';
</script>

<Wrapper>
	<Header />
	<slot />
</Wrapper>

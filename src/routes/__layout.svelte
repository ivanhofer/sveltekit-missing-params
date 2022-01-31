<script context="module" lang="ts">
	import type { Load } from '@sveltejs/kit'

	type LoadInput = {
		pageParams: { slug?: string }
	}

	export const load: Load<LoadInput> = async ({ url, params }) => {
		return {
			props: {
				pathName: url.pathname,
				slug: params.slug,
			},
		}
	}
</script>

<script lang="ts">
	export let pathName: string
	export let slug: string
</script>

<p>url-path: {pathName}</p>
<p>[slug]: {slug}</p>

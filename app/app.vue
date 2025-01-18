<script setup lang="ts">
const settings = useSettings()

const showModal = ref(false)

useMagicKeys({
	passive: false,
	onEventFired(e) {
		if (e.metaKey && e.key === ',' && e.type === 'keydown') {
			e.preventDefault()
			showModal.value = true
			return
		}

		if (e.key === 'Escape' && e.type === 'keydown' && showModal.value) {
			e.preventDefault()
			showModal.value = false
		}
	},
})

if (import.meta.client) {
	settings.userAgent = detectUserAgent()
}
</script>

<template>
	<NuxtRouteAnnouncer />
	<SvgSprite />

	<main class="flex flex-col flex-1 relative">
		<BaseButton
			class="absolute top-4 right-4"
			@click="showModal = true"
		>
			Settings
		</BaseButton>
		<article class="mx-auto flex w-full max-w-2xl flex-1 flex-col gap-y-16 p-4">
			<TimeController @show-settings="showModal = true" />
			<TodoController />
		</article>
		<LazyBaseModal v-model="showModal">
			<SiteSettings />
		</LazyBaseModal>
	</main>
</template>

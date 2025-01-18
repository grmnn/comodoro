<template>
	<ul class="text-xs text-zinc-500 flex flex-col gap-y-4">
		<li class="flex items-center gap-x-2 justify-between">
			<span><BaseKbd key-label="Space" /></span>
			<span>Start / Stop timer</span>
		</li>
		<li class="flex items-center gap-x-2 justify-between ">
			<span><BaseKbd key-label="meta" /> <BaseKbd key-label="," /></span>
			<span>Open Settings</span>
		</li>
		<li class="flex items-center gap-x-2 justify-between">
			<span><BaseKbd key-label="meta" /> <BaseKbd key-label="F" /></span>
			<span>Focus Todo Input</span>
		</li>
		<li class="flex items-center gap-x-2 justify-between">
			<span><BaseKbd key-label="↑" /> <BaseKbd key-label="↓" /></span>
			<span>Navigate Between Todos</span>
		</li>
		<li class="flex items-center gap-x-2 justify-between">
			<span><BaseKbd key-label="Enter" /></span>
			<span>Toggle Focused Todo</span>
		</li>
		<li class="flex items-center gap-x-2 justify-between">
			<span><BaseKbd key-label="meta" /> <BaseKbd key-label="⌫" /></span>
			<span>Delete Focused Todo</span>
		</li>

		<li class="flex items-center gap-x-2 justify-between">
			<span><BaseKbd key-label="Alt" /> <BaseKbd key-label="↑" /></span>
			<span>Move Focused Todo Up</span>
		</li>
		<li class="flex items-center gap-x-2 justify-between">
			<span><BaseKbd key-label="Alt" /> <BaseKbd key-label="↓" /></span>
			<span>Move Focused Todo Down</span>
		</li>
	</ul>
</template>

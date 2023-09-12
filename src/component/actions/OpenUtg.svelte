<script lang="ts">
	let openPosition = 'openUtg';

	function Position(position: string) {
		openPosition = position;
		return {
			openPosition
		};
	}
</script>

<!-- botnera y foto -->
<div class="container flex flex-row">
	<!-- botonera -->
	<div class="container flex flex-col text-center w-20 m-2 gap-5 border-solid- border-2">
		<h1 class="text-sm">Open UTG</h1>
		<button
			class="rounded-full bg-cyan-700 w-20 hover:bg-cyan-500 focus:outline-none
						focus:ring-2 focus:ring-blue-400 focus:ring-opacity-75 text-sm"
			on:click={() => Position('openUtg')}
			>OPEN
		</button>

		<button
			class="rounded-full bg-cyan-700 w-20 hover:bg-cyan-500 focus:outline-none
						focus:ring-2 focus:ring-blue-400 focus:ring-opacity-75 text-sm"
			on:click={() => Position('vs3betOop')}
			>vs 3BET OOP
		</button>
	</div>
	<!-- foto -->
	<div class="container flex border-solid- border-2 justify-center items-center">
		{#if openPosition == 'openUtg'}
			<!-- content here -->
			<img src="../src/lib/img/openUtg.jpg" width="400" height="400" alt="open utg" />
		{/if}
		{#if openPosition == 'vs3betOop'}
			<!-- content here -->
			<img src="../src/lib/img/vs3betOop.jpg" width="400" height="400" alt=" vs 3bet oop" />
		{/if}
	</div>
</div>

<script lang="ts">
	let openPosition = 'openSb';

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
		<h1 class="text-sm">Open SB</h1>
		<button
			class="rounded-full bg-cyan-700 w-20 hover:bg-cyan-500 focus:outline-none
						focus:ring-2 focus:ring-blue-400 focus:ring-opacity-75 text-sm"
			on:click={() => Position('openSb')}
			>OPEN
		</button>

		<button
			class="rounded-full bg-cyan-700 w-20 hover:bg-cyan-500 focus:outline-none
						focus:ring-2 focus:ring-blue-400 focus:ring-opacity-75 text-sm"
			on:click={() => Position('sbVsEarly')}
			>SB vs Early
		</button>
		<button
			class="rounded-full bg-cyan-700 w-20 hover:bg-cyan-500 focus:outline-none
						focus:ring-2 focus:ring-blue-400 focus:ring-opacity-75 text-sm"
			on:click={() => Position('sbVsCu')}
			>SB vs CU
		</button>
		<button
			class="rounded-full bg-cyan-700 w-20 hover:bg-cyan-500 focus:outline-none
						focus:ring-2 focus:ring-blue-400 focus:ring-opacity-75 text-sm"
			on:click={() => Position('sbVsBtn')}
			>SB vs BTN
		</button>
		<button
			class="rounded-full bg-cyan-700 w-20 hover:bg-cyan-500 focus:outline-none
						focus:ring-2 focus:ring-blue-400 focus:ring-opacity-75 text-sm"
			on:click={() => Position('sqzVsEarly&Co')}
			>SQZ vs Early & CU
		</button>
		<button
			class="rounded-full bg-cyan-700 w-20 hover:bg-cyan-500 focus:outline-none
						focus:ring-2 focus:ring-blue-400 focus:ring-opacity-75 text-sm"
			on:click={() => Position('sqzVsCo&Btn')}
			>SQZ vs CU & BTN
		</button>
		<button
			class="rounded-full bg-cyan-700 w-20 hover:bg-cyan-500 focus:outline-none
						focus:ring-2 focus:ring-blue-400 focus:ring-opacity-75 text-sm"
			on:click={() => Position('rol')}
			>ROL
		</button>
	</div>
	<!-- foto -->
	<div class="container flex border-solid- border-2 justify-center items-center">
		{#if openPosition == 'openSb'}
			<!-- content here -->
			<img src="../src/lib/img/openSb.jpg" width="400" height="400" alt="open utg" />
		{/if}
		{#if openPosition == 'sbVsEarly'}
			<!-- content here -->
			<img src="../src/lib/img/sbVsEarly.jpg" width="400" height="400" alt=" vs 3bet oop" />
		{/if}
		{#if openPosition == 'sbVsCu'}
			<!-- content here -->
			<img src="../src/lib/img/sbVsCu.jpg" width="400" height="400" alt=" vs 3bet oop" />
		{/if}
		{#if openPosition == 'sbVsBtn'}
			<!-- content here -->
			<img src="../src/lib/img/sbVsBtn.jpg" width="400" height="400" alt=" vs 3bet oop" />
		{/if}
		{#if openPosition == 'sqzVsEarly&Co'}
			<!-- content here -->
			<img src="../src/lib/img/sbVsEarlyVsCu.jpg" width="400" height="400" alt=" vs 3bet oop" />
		{/if}
		{#if openPosition == 'sqzVsCo&Btn'}
			<!-- content here -->
			<img src="../src/lib/img/svVsCuVsBtn.jpg" width="400" height="400" alt=" vs 3bet oop" />
		{/if}
		{#if openPosition == 'rol'}
			<!-- content here -->
			<img src="../src/lib/img/rolSb.jpg" width="400" height="400" alt=" vs 3bet oop" />
		{/if}
	</div>
</div>

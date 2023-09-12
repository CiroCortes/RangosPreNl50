<script lang="ts">
	let openPosition = 'openBtn';

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
		<h1 class="text-sm">Open BTN</h1>
		<button
			class="rounded-full bg-cyan-700 w-20 hover:bg-cyan-500 focus:outline-none
						focus:ring-2 focus:ring-blue-400 focus:ring-opacity-75 text-sm"
			on:click={() => Position('openBtn')}
			>OPEN
		</button>

		<button
			class="rounded-full bg-cyan-700 w-20 hover:bg-cyan-500 focus:outline-none
						focus:ring-2 focus:ring-blue-400 focus:ring-opacity-75 text-sm"
			on:click={() => Position('btnVsEarly')}
			>BTN vs Early
		</button>
		<button
			class="rounded-full bg-cyan-700 w-20 hover:bg-cyan-500 focus:outline-none
						focus:ring-2 focus:ring-blue-400 focus:ring-opacity-75 text-sm"
			on:click={() => Position('btnVsCu')}
			>BTN vs CU
		</button>
		<button
			class="rounded-full bg-cyan-700 w-20 hover:bg-cyan-500 focus:outline-none
						focus:ring-2 focus:ring-blue-400 focus:ring-opacity-75 text-sm"
			on:click={() => Position('sqz')}
			>SQZ
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
		{#if openPosition == 'openBtn'}
			<!-- content here -->
			<img src="../src/lib/img/openBtn.jpg" width="400" height="400" alt="open utg" />
		{/if}
		{#if openPosition == 'btnVsEarly'}
			<!-- content here -->
			<img src="../src/lib/img/btnVsEarly.jpg" width="400" height="400" alt=" vs 3bet oop" />
		{/if}
		{#if openPosition == 'btnVsCu'}
			<!-- content here -->
			<img src="../src/lib/img/btnVsCu.jpg" width="400" height="400" alt=" vs 3bet oop" />
		{/if}
		{#if openPosition == 'sqz'}
			<!-- content here -->
			<img src="../src/lib/img/btnSqz.jpg" width="400" height="400" alt=" vs 3bet oop" />
		{/if}
		{#if openPosition == 'rol'}
			<!-- content here -->
			<img src="../src/lib/img/btnRol.jpg" width="400" height="400" alt=" vs 3bet oop" />
		{/if}
	</div>
</div>

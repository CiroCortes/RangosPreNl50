<script lang="ts">
	let openPosition = 'bbVsEarly';
	let openMenu = false;

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
	<div class="container flex flex-col text-center w-60 m-2 gap-5 border-solid- border-2">
		<h1 class="text-sm">BB GAME</h1>

		<div class="container flex flex-col text-center w-20 m-2 gap-5 border-solid- border-2">
			<button
				class="rounded-full bg-cyan-700 w-20 hover:bg-cyan-500 focus:outline-none
						focus:ring-2 focus:ring-blue-400 focus:ring-opacity-75 text-sm"
				on:click={() => Position('bbVsEarly')}
				>BB vs Early
			</button>

			<button
				class="rounded-full bg-cyan-700 w-20 hover:bg-cyan-500 focus:outline-none
						focus:ring-2 focus:ring-blue-400 focus:ring-opacity-75 text-sm"
				on:click={() => Position('bbVsCu')}
				>BB vs CU
			</button>
			<button
				class="rounded-full bg-cyan-700 w-20 hover:bg-cyan-500 focus:outline-none
						focus:ring-2 focus:ring-blue-400 focus:ring-opacity-75 text-sm"
				on:click={() => Position('bbVsBtn')}
				>BB vs BTN
			</button>
			<button
				class="rounded-full bg-cyan-700 w-20 hover:bg-cyan-500 focus:outline-none
						focus:ring-2 focus:ring-blue-400 focus:ring-opacity-75 text-sm"
				on:click={() => Position('bbVsSb')}
				>BB vs SB
			</button>
			<button
				class="rounded-full bg-cyan-700 w-20 hover:bg-cyan-500 focus:outline-none
						focus:ring-2 focus:ring-blue-400 focus:ring-opacity-75 text-sm"
				on:click={() => Position('rol')}
				>ROL
			</button>
			<button
				class="rounded-full bg-cyan-700 w-20 hover:bg-cyan-500 focus:outline-none
						focus:ring-2 focus:ring-blue-400 focus:ring-opacity-75 text-sm"
				on:click={() => Position('rolVsSb')}
				>ROL vs SB
			</button>
		</div>

		<button
			class="rounded-full bg-cyan-700 w-40 hover:bg-cyan-500 focus:outline-none
						focus:ring-2 focus:ring-blue-400 focus:ring-opacity-75 text-sm"
			on:click={() => (openMenu = !openMenu)}
			>Multiway
		</button>

		<!-- multyway -->
		{#if openMenu}
			<div class="container flex flex-row w-40 m-2 gap-5 border-solid- border-2">
				<button
					class="rounded-full bg-cyan-700 w-20 hover:bg-cyan-500 focus:outline-none
						focus:ring-2 focus:ring-blue-400 focus:ring-opacity-75 text-xs"
					on:click={() => Position('sqzVsEarlyMi&Co')}
					>vs Ear. & MI/CU
				</button>
				<button
					class="rounded-full bg-cyan-700 w-20 hover:bg-cyan-500 focus:outline-none
						focus:ring-2 focus:ring-blue-400 focus:ring-opacity-75 text-xs"
					on:click={() => Position('sqzVsEar&Btn')}
					>vs Ear. & BTN
				</button>
			</div>
			<div class="container flex flex-row w-40 m-2 gap-5 border-solid- border-2">
				<button
					class="rounded-full bg-cyan-700 w-20 hover:bg-cyan-500 focus:outline-none
						focus:ring-2 focus:ring-blue-400 focus:ring-opacity-75 text-xs"
					on:click={() => Position('sqzVsEarly&Sb')}
					>vs Ear. & SB
				</button>
				<button
					class="rounded-full bg-cyan-700 w-20 hover:bg-cyan-500 focus:outline-none
                    focus:ring-2 focus:ring-blue-400 focus:ring-opacity-75 text-sm"
					on:click={() => Position('sqzVsCo&Btn')}
					>vs CO & BTN
				</button>
			</div>
			<div class="container flex flex-row w-40 m-2 gap-5 border-solid- border-2">
				<button
					class="rounded-full bg-cyan-700 w-20 hover:bg-cyan-500 focus:outline-none
						focus:ring-2 focus:ring-blue-400 focus:ring-opacity-75 text-sm"
					on:click={() => Position('sqzVsCo&Sb')}
					>vs CO & SB
				</button>
				<button
					class="rounded-full bg-cyan-700 w-20 hover:bg-cyan-500 focus:outline-none
						focus:ring-2 focus:ring-blue-400 focus:ring-opacity-75 text-sm"
					on:click={() => Position('sqzVsBtn&Sb')}
					>vs BTN & SB
				</button>
			</div>
		{/if}
	</div>
	<!-- foto -->
	<div class="container flex border-solid- border-2 justify-center items-center">
		{#if openPosition == 'bbVsEarly'}
			<!-- content here -->
			<img src="../src/lib/img/bbgames/bbVsEarly.jpg" width="400" height="400" alt="open utg" />
		{/if}
		{#if openPosition == 'bbVsCu'}
			<!-- content here -->
			<img src="../src/lib/img/bbgames/bbVsCu.jpg" width="400" height="400" alt=" vs 3bet oop" />
		{/if}
		{#if openPosition == 'bbVsBtn'}
			<!-- content here -->
			<img src="../src/lib/img/bbgames/bbVsBtn.jpg" width="400" height="400" alt=" vs 3bet oop" />
		{/if}
		{#if openPosition == 'bbVsSb'}
			<!-- content here -->
			<img src="../src/lib/img/bbgames/bbVsSb.jpg" width="400" height="400" alt=" vs 3bet oop" />
		{/if}
		{#if openPosition == 'rol'}
			<!-- content here -->
			<img src="../src/lib/img/bbgames/rolBBoop.jpg" width="400" height="400" alt=" vs 3bet oop" />
		{/if}
		{#if openPosition == 'rolVsSb'}
			<!-- content here -->
			<img
				src="../src/lib/img/bbgames/rolBBvsSBx4.jpg"
				width="400"
				height="400"
				alt=" vs 3bet oop"
			/>
		{/if}
		<!--MULTIWAY IFES-->
		{#if openPosition == 'sqzVsEarlyMi&Co'}
			<!-- content here -->
			<img
				src="../src/lib/img/bbgames/sqzbb/vsEarlyMiCu.jpg"
				width="400"
				height="400"
				alt=" vs 3bet oop"
			/>
		{/if}
		{#if openPosition == 'sqzVsEar&Btn'}
			<!-- content here -->
			<img
				src="../src/lib/img/bbgames/sqzbb/vsEarlyBtn.jpg"
				width="400"
				height="400"
				alt=" vs 3bet oop"
			/>
		{/if}
		{#if openPosition == 'sqzVsEarly&Sb'}
			<!-- content here -->
			<img
				src="../src/lib/img/bbgames/sqzbb/vsEarlySb.jpg"
				width="400"
				height="400"
				alt=" vs 3bet oop"
			/>
		{/if}
		{#if openPosition == 'sqzVsCo&Btn'}
			<!-- content here -->
			<img
				src="../src/lib/img/bbgames/sqzbb/vsCoYbTN.jpg"
				width="400"
				height="400"
				alt=" vs 3bet oop"
			/>
		{/if}
		{#if openPosition == 'sqzVsCo&Sb'}
			<!-- content here -->
			<img
				src="../src/lib/img/bbgames/sqzbb/vsCoySb.jpg"
				width="400"
				height="400"
				alt=" vs 3bet oop"
			/>
		{/if}
		{#if openPosition == 'sqzVsBtn&Sb'}
			<!-- content here -->
			<img
				src="../src/lib/img/bbgames/sqzbb/vsBtnySb.jpg"
				width="400"
				height="400"
				alt=" vs 3bet oop"
			/>
		{/if}
	</div>
</div>

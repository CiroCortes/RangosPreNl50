<!-- YOU CAN DELETE EVERYTHING IN THIS PAGE -->
<script lang="ts">
	import GameBigBlind from '../component/actions/GameBigBlind.svelte';
	import OpenBtn from '../component/actions/OpenBtn.svelte';
	import OpenCo from '../component/actions/OpenCo.svelte';
	import OpenMp from '../component/actions/OpenMp.svelte';
	import OpenSb from '../component/actions/OpenSb.svelte';
	import OpenUtg from '../component/actions/OpenUtg.svelte';

	let openposition = 'UTG';

	function ChangePosition(realPosition: string) {
		openposition = realPosition;
	}
</script>

<div class="container h-full mx-auto flex-col justify-center items-center">
	<h1 class=" w-full border-solid border-2 flex justify-center items-center">
		Rangos y acciones Preflop
	</h1>
	<div class="container w-full flex flex-row">
		<div class="max-w-screen border-solid border-2 flex-grow">
			<h1 class="flex justify-center items-center">seccion rangos</h1>
			<!--seccion de acciones completo-->
			<div class="container w-full flex flex-row border-solid border-2">
				<!--seccion de botones posicion-->
				<div class="container flex flex-col text-center w-20 m-2 gap-5 border-solid- border-2">
					<button
						class="rounded-full bg-cyan-700 hover:bg-cyan-500 focus:outline-none
						focus:ring-2 focus:ring-blue-400 focus:ring-opacity-75"
						on:click={() => ChangePosition('UTG')}
					>
						UTG
					</button>
					<button
						class="rounded-full bg-cyan-700 w-20 hover:bg-cyan-500 focus:outline-none
						focus:ring-2 focus:ring-blue-400 focus:ring-opacity-75"
						on:click={() => ChangePosition('MP')}
					>
						MP
					</button>
					<button
						class="rounded-full bg-cyan-700 w-20 hover:bg-cyan-500 focus:outline-none
						focus:ring-2 focus:ring-blue-400 focus:ring-opacity-75"
						on:click={() => ChangePosition('CO')}
					>
						CO
					</button>
					<button
						class="rounded-full bg-cyan-700 w-20 hover:bg-cyan-500 focus:outline-none
						focus:ring-2 focus:ring-blue-400 focus:ring-opacity-75"
						on:click={() => ChangePosition('BTN')}
					>
						BTN
					</button>
					<button
						class="rounded-full bg-cyan-700 w-20 hover:bg-cyan-500 focus:outline-none
						focus:ring-2 focus:ring-blue-400 focus:ring-opacity-75"
						on:click={() => ChangePosition('SB')}
					>
						SB
					</button>
					<button
						class="rounded-full bg-cyan-700 w-20 hover:bg-cyan-500 focus:outline-none
						focus:ring-2 focus:ring-blue-400 focus:ring-opacity-75"
						on:click={() => ChangePosition('BB')}
					>
						BB
					</button>
				</div>
				<!--seccion de botones accion UTG-->
				<div class="container flex text-center w-50 m-2 gap-5 border-solid- border-2 items-center">
					{#if openposition == 'UTG'}
						<!-- content here -->
						<OpenUtg />
					{/if}
					{#if openposition == 'MP'}
						<!-- content here -->
						<OpenMp />
					{/if}
					{#if openposition == 'CO'}
						<!-- content here -->
						<OpenCo />
					{/if}
					{#if openposition == 'BTN'}
						<!-- content here -->
						<OpenBtn />
					{/if}
					{#if openposition == 'SB'}
						<!-- content here -->
						<OpenSb />
					{/if}
					{#if openposition == 'BB'}
						<!-- content here -->
						<GameBigBlind />
					{/if}
				</div>
			</div>
		</div>
		<div class="max-w-screen border-solid border-2 flex-grow">
			<h1 class="flex justify-center items-center">Tipo de FLOP</h1>
		</div>
	</div>
</div>

<script>

	import Chip, {Set, Checkmark, Text} from '@smui/chips';
	
	import  {Label} from '@smui/button';
	import Tab from '@smui/tab';
	import TabBar from '@smui/tab-bar';

	import StylesData from './components/StylesData.svelte';
	import PyData from './components/PyData.svelte';
	import JsData from './components/JsData.svelte';
	import SvelteCards from './components/SvelteCards.svelte';

  const options = [
	  {name: 'styles', component: StylesData},
	  {name: 'python', component: PyData},
	  {name: 'JavaScript', component:JsData},
	  {name: 'Svelte', component:SvelteCards}
  ];
 
  let choice = options[0];

</script>


<div class="container">

	<div class="box header">
		<Set chips={options} let:chip choice bind:selected={choice}>
			<Chip tabindex="0">{chip.name}</Chip>
		</Set>
	</div>

	<div class="box content">
	  <svelte:component this={choice.component}/>
	</div>

	<div class="box footer">Footer</div>
</div>


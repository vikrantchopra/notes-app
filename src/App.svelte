<script>
	export let name;

	import Card, {Content, PrimaryAction, Media, MediaContent, Actions, ActionButtons, ActionIcons} from '@smui/card'
	import Button, {Label} from '@smui/button';
	import IconButton, {Icon} from '@smui/icon-button';
	import Tab from '@smui/tab';
	import TabBar from '@smui/tab-bar';

	import StylesData from './components/StylesData.svelte';
	import PyData from './components/PyData.svelte';
	import CardData from './components/CardData.svelte';

	function doAction(action) {
		alert('You did an action ' + action);
	}
	
	let iconTabs = [
    {
      icon: 'access_time',
      label: 'Recents'
    },
    {
      icon: 'near_me',
      label: 'Nearby'
    },
    {
      icon: 'favorite',
      label: 'Favorites'
    }
  ];

  let iconTab = iconTabs[2];
  let active = 'Home';

  const options = [
	  {name: 'styles', component: StylesData},
	   {name: 'pandas', component: PyData},
  ];
  let selected = options[0];

</script>


<div class="container">
	
	<div class="box header">
		<TabBar tabs={options} let:tab bind:active={selected}>
			<Tab {tab}>
				
				<Label>{tab.name}</Label>
			</Tab>
		</TabBar>
		
	</div>

	<div class="box content">
	  <svelte:component this={selected.component}/>
	</div>


	<div class="box footer">Footer</div>
</div>


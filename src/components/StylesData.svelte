<script>
	import Card, {Content, PrimaryAction, Media, MediaContent, Actions, ActionButtons, ActionIcons} from '@smui/card'
	import Button, {Label} from '@smui/button';
	import IconButton, {Icon} from '@smui/icon-button';

    let cssCards = [
		{
			header: 'Learning Grid',
			content: 'Grid is a new feature introduced in css3 that helps in page layout by using both the x and y axis effectively',
			resource: 'flexgrid.com/theholygrail'
		},
		{
			header: 'Learning flexbox',
			content: 'Flex box is helpful for laying out items or components either horizontally or vertically',
			resource: 'flexfroggy.com/flexboxtutorial'
		},
		{
			header: 'Layout with Grid',
			content: 'Redefining grid layout with grid area and media queries',
			resource: 'gridbyexample.com'
		}
	];

</script>

{#each cssCards as {header, content, resource}}
	<Card>
		<div style="padding: 1rem;">
			<h2 class="mdc-typography--headline5" style="margin: 0;">{header}</h2>
		</div>
		
		<Content class="mdc-typography--body2 card-content">
			{content}
			
		</Content>
		<h5 class="mdc-typography--body2" style="padding: 1rem; ">{resource}</h5>
	</Card>
{/each}
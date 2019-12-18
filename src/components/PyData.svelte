<script>
	import Card, {Content, PrimaryAction, Media, MediaContent, Actions, ActionButtons, ActionIcons} from '@smui/card'
	import Button, {Label} from '@smui/button';
	import IconButton, {Icon} from '@smui/icon-button';
	

    let pyCards = [
		{
			header: 'Pandas',
			content: 'Pandas are an excellent way analysing, crunching and displaying humongous datasets',
			resource: 'google.com'
		},
		{
			header: 'Bokeh',
			content: 'Bokeh is an excellent library for visualization of dynamic data',
			resource: 'google.com'
		},
		{
			header: 'Using Python  to get Robinhood Data',
			content: 'Lets automate some stocks, can be used to build a trading robot',
			resource: 'towardsdatascience.com'
		}
    ];
    
</script>

 {#each pyCards as {header, content, resource}}
	<Card>
		<div style="padding: 1rem;">
			<h2 class="mdc-typography--headline6" style="margin: 0;">{header}</h2>
		</div>
		
		<Content class="mdc-typography--body2">{content}</Content>
		<h4>{resource}</h4>
	</Card>
{/each}
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
			header: 'Robinhood Data with Python',
			content: 'Lets automate some stocks, can be used to build a trading robot',
			resource: 'towardsdatascience.com'
		}
    ];
    
</script>

 {#each pyCards as {header, content, resource}}
	<Card>
		<div style="padding: 1rem;">
			<h2 class="mdc-typography--headline5" style="margin: 0;">{header}</h2>
		</div>
		
		<Content class="mdc-typography--body2 card-content">{content}</Content>
		<h5 class="mdc-typography--body2" style="padding: 1rem; ">{resource}</h5>
	</Card>
{/each}
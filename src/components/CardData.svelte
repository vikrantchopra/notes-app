<script>
    import Card, {Content, PrimaryAction, Media, MediaContent, Actions, ActionButtons, ActionIcons} from '@smui/card'
	import Button, {Label} from '@smui/button';
    import IconButton, {Icon} from '@smui/icon-button';
    
    let clicked = 0;

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
		}
	];
</script>


		<Card style="">
        <div style="padding: 1rem;">
          <h2 class="mdc-typography--headline6" style="margin: 0;">A card with media.</h2>
          <h3 class="mdc-typography--subtitle2" style="margin: 0; color: #888;">And a subtitle.</h3>
        </div>
        <PrimaryAction on:click={() => clicked++}>
          <Media class="card-media-16x9" aspectRatio="16x9"></Media>
          <Content class="mdc-typography--body2">
            And some info text. And it's a primary action for the card.
          </Content>
        </PrimaryAction>
      </Card>

	  {#each pyCards as {header, content, resource}}
		<Card>
			<div style="padding: 1rem;">
				<h2 class="mdc-typography--headline6" style="margin: 0;">{header}</h2>
			</div>
			
			<Content class="mdc-typography--body2">{content}</Content>
			<h4>{resource}</h4>
		</Card>
	  {/each}

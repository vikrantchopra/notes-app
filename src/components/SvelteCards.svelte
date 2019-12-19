<script>
    import Card, {Content, PrimaryAction, Media, MediaContent, Actions, ActionButtons, ActionIcons} from '@smui/card'
	import Button, {Label} from '@smui/button';
	import IconButton, {Icon} from '@smui/icon-button';

    let svelteCards = [
        {
            header: 'Configure Svelte with Material UI',
            content: [
                {id: 1, bullet: 'Create svelte app: npx degit sveltejs/template APP-NAME'},
                {id: 2, bullet: 'cd APP-NAME & npm install or yarn install'},
                {id: 3, bullet: 'npm install --save-dev svelte-preprocess node-sass @material/typography rollup-plugin-postcss' + 
                    '<br/> &emsp; OR <br/> &nbsp yarn add --dev svelte-preprocess node-sass @material/typography rollup-plugin-postcss'},
                {id: 4, bullet: 'create App.scss in the src folder'},
                {id: 5, bullet: 'create a folder called theme. Inside theme create an empty file _smui-theme.scss'},
                {id: 6, bullet: 'inside rollup.config.js ' + 
                        '  <br/>import postcss from "rollup-plugin-postcss"; ' + 
                        ' <br/>import autoPreprocess from "svelte-preprocess";' + 
                        ' <br/>add preprocess: autoPreprocess() inside plugin->svelte block'}
            ]
            
        },
         {
            header: 'An introduction to Svelte',
             content: [
                {id: 1, bullet: 'Create svelte app: npx degit sveltejs/template APP-NAME'},
                {id: 2, bullet: 'cd APP-NAME & npm install or yarn install'}
            ]
        },
         {
            header: 'Svelte with Material UI',
            content: [
                {id: 1, bullet: 'Create svelte app: npx degit sveltejs/template APP-NAME'},
                {id: 2, bullet: 'cd APP-NAME & npm install or yarn install'}
            ]
        },
    ];
</script>

{#each svelteCards as {header, content}}
	<Card>
		<div style="padding: 1rem;">
			<h2 class="mdc-typography--headline5" style="margin: 0;">{header}</h2>
		</div>
		
		<Content class="mdc-typography--body2">
            {#each content as {id, bullet}}
			   <strong>{id}: </strong> {@html bullet} <br/>
			{/each}
		</Content>
		
	</Card>
{/each}
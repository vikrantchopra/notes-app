<script>
	import Card, {Content, PrimaryAction, Media, MediaContent, Actions, ActionButtons, ActionIcons} from '@smui/card'
	import Button, {Label} from '@smui/button';
	import IconButton, {Icon} from '@smui/icon-button';

    let jsCards = [
		{
			header: 'Vanilla JS before JS Frameworks',
			content: 'If you master JavaScript fundamentals, your only challenge when learning new JS frameworks will be scoped to their specific syntax',
			resource: 'https://snipcart.com/blog/learn-vanilla-javascript-before-using-js-frameworks'
		},
		{
			header: 'Making SPA in ye goold olde JS',
			content: 'The article underscores the futility of using JS frameworks for front end development. Plain JS is good enough and a whole lot easier',
			resource: 'https://dev.to/rishavs/making-a-single-page-app-in-ye-good-olde-js-es6-3eng'
		},
		{
			header: 'Pretending to Know Javascript',
			content: 'With  the surfeit of JS frameworks and eagerness to learn those, the new breed of developers is forgetting plain JavaScript. They are missing an opportunity to be a great front end developer',
			resource: 'O Reilly - Book, The Definitive Guide'
		}
	];

</script>

{#each jsCards as {header, content, resource}}
	<Card>
		<div style="padding: 1rem;">
			<h2 class="mdc-typography--headline6" style="margin: 0;">{header}</h2>
		</div>
		
		<Content class="mdc-typography--body2 card-content">{content}</Content>
		<h5 class="" style="padding: 1rem; font-size: 0.7rem;">{resource}</h5>
	</Card>
{/each}
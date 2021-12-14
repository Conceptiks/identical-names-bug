<script>

    import { page } from '$app/stores';

	let components = [
		{
			group: 'info',
			content: ['installation']
		},
		{
			group: 'atoms',
			content: ['button']
		}
	];

	const createStructure = () => {
		let structure = [];

		components.forEach((comp) => {
			const componentType = comp.group;
			let items = [];

			comp.content.forEach((componentName) => {
				let path = `/${componentType}/${componentName}`;
				items.push({
					path: path,
					name: componentName
				});
			});

			structure.push({
				type: componentType,
				items: items
			});
		});

		return structure;
	};
</script>

{#each createStructure() as componentGroup}
	<div>
		<div>{componentGroup.type}</div>
		<ul>
			{#each componentGroup.items as component}
				<li class:active={$page.path === component.path}>
					<a href={component.path}>{component.name}</a>
				</li>
			{/each}
		</ul>
	</div>
{/each}

<slot></slot>

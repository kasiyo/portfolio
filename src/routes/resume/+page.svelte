<script lang="ts">
	import { LocationFilled, LogoGithub, Email, PhoneFilled } from 'carbon-icons-svelte';

	const personal = [
		{
			icon: LocationFilled,
			text: 'Dallas-Fort Worth, TX',
			size: 32
		},
		{
			icon: LogoGithub,
			text: '@kasiyo'
		},
		{
			icon: Email,
			text: 'kaiasiripanyo@gmail.com'
		},
		{
			icon: PhoneFilled,
			text: '(817) 707-3386'
		}
	];
</script>

<header>
	<a href="/">home</a>
</header>

<article class="resume-doc container grid grid-cols-12">
	<div id="resume-heading" class="col-start-2">
		<h1 class="text-6xl tracking-wider col-span-3">Kaia Siripanyo</h1>
	</div>

	<section id="personal-data" class="col-start-7 col-span-5 flex flex-row">
		<ul class="badge-list mx-5">
			{#each personal as { icon, text }}
				<li>
					<svelte:component this={icon} size={32} font-size={10} />
					{text}
				</li>

				<br />
			{/each}
		</ul>
	</section>
	<div class="row-start-3 col-start-7 col-span-5 flex flex-row">
		<ul class="badge-list">
			<li>
				<LocationFilled size={32} />
				<span class="subpixel-antialiased col-start-10">Dallas-Fort Worth, TX</span>
			</li>
			<li>
				<LogoGithub size={32} class="col-start-9 col-span-1" />
				<span class="subpixel-antialiased col-start-10">@kasiyo</span>
			</li>
			<li>
				<Email size={32} />
				<span class="subpixel-antialiased ml-3">kaiasiripanyo@gmail.com</span>
			</li>
			<li>
				<PhoneFilled size={32} />
				<span class="subpixel-antialiased">(817) 707-3386</span>
			</li>
		</ul>
	</div>
</article>

<nav>
    <div class="nav-container">
        <a href="/" class="nav-logo" title="Back to Homepage">Андрей Кузнецов</a>
        <div class="nav-links">
            {#each nav as link}
				{#if link.isShow}
				<a href={link.href} class="link">{link.title}</a>
				{/if}
            {/each}
        </div>
    </div>
</nav>

<div class="container">
    <!-- Pages will be injected below -->
    <slot></slot>
</div>
<script>
    	const nav = [
		{
			title: 'Обо мне',
			href: '/about',
			isShow: true
		},
		{
			title: 'Блог',
			href: '/blog',
			isShow: true
		},
		{
			title: 'Портфолио',
			href: '/project',
			isShow: true
		},
		{
			title: 'Контакты',
			href: '/contact',
			isShow: true
		},
        {
			title: 'temp',
			href: '/temp',
			isShow: false
		}
	]
</script>
<style>
       .container {
           margin: 50px auto;
           max-width: 800px;
           padding: 0 20px;
       }
</style>

<script>
    import {toggleMode} from "mode-watcher";
    import {Share} from "lucide-svelte";
    import Sun from "lucide-svelte/icons/sun";
    import Moon from "lucide-svelte/icons/moon";
    import {Button} from "$lib/components/ui/button/index.ts";
</script>

<header class="sticky top-0 z-10 flex items-center gap-1 border-b px-4 h-[57px] bg-background">
	<h1 class="text-xl font-semibold">Dashboard</h1>
	<Button variant="outline"
	        size="sm"
	        class="ml-auto text-sm gap-1.5">
		<Share class="size-3.5" />
		Share
	</Button>
	<Button on:click={toggleMode}
	        variant="outline"
	        size="sm">
		<Sun class="rotate-0 scale-100 transition-all h-[1.2rem] w-[1.2rem] dark:-rotate-90 dark:scale-0" />
		<Moon class="absolute rotate-90 scale-0 transition-all h-[1.2rem] w-[1.2rem] dark:rotate-0 dark:scale-100" />
		<span class="sr-only">Toggle theme</span>
	</Button>
</header>
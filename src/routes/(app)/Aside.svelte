<script>
    import * as Tooltip from "$lib/components/ui/tooltip/index.ts";
    import {Button} from "$lib/components/ui/button/index.ts";
    import {Triangle} from "lucide-svelte";
    import {Bot} from "lucide-svelte";
    import {SquareTerminal} from "lucide-svelte";
    import {CodeXml} from "lucide-svelte";
    import {Settings2} from "lucide-svelte";
    import {SquareUser} from "lucide-svelte";
    import {page} from "$app/stores";
</script>
<aside class="fixed left-0 z-20 flex h-full flex-col border-r inset-y">
	<div class="border-b p-2">
		<Button variant="outline"
		        size="icon"
		        aria-label="Home">
			<Triangle class="size-5 fill-foreground" />
		</Button>
	</div>
	<nav class="grid gap-1 p-2">
		<!-- ADD -->
		<Tooltip.Root>
			<Tooltip.Trigger asChild
			                 let:builder>
				<Button variant="ghost"
				        size="icon"
				        class="rounded-lg aria-[current='page']:bg-muted transition-colors"
				        aria-label="Elemente"
				        aria-current="{$page.url.pathname === '/add' ? 'page' : undefined}"
				        builders={[builder]}
				        href="/add">
					<SquareTerminal class="size-5" />
				</Button>
			</Tooltip.Trigger>
			<Tooltip.Content side="right"
			                 sideOffset={5}>Element hinzufügen
			</Tooltip.Content>
		</Tooltip.Root>
		<!-- EDIT -->
		<Tooltip.Root>
			<Tooltip.Trigger asChild
			                 let:builder>
				<Button variant="ghost"
				        size="icon"
				        class="rounded-lg aria-[current='page']:bg-muted transition-colors"
				        aria-label="Edit"
				        aria-current="{$page.url.pathname === '/edit' ? 'page' : undefined}"
				        builders={[builder]}
				        href="/edit">
					<Bot class="size-5" />
				</Button>
			</Tooltip.Trigger>
			<Tooltip.Content side="right"
			                 sideOffset={5}>Bearbeiten
			</Tooltip.Content>
		</Tooltip.Root>
		<!-- STYLE -->
		<Tooltip.Root>
			<Tooltip.Trigger asChild
			                 let:builder>
				<Button variant="ghost"
				        size="icon"
				        class="rounded-lg aria-[current='page']:bg-muted transition-colors"
				        aria-label="Style"
				        aria-current="{$page.url.pathname === '/style' ? 'page' : undefined}"
				        builders={[builder]}
				        href="/style">
					<CodeXml class="size-5" />
				</Button>
			</Tooltip.Trigger>
			<Tooltip.Content side="right"
			                 sideOffset={5}>Styling
			</Tooltip.Content>
		</Tooltip.Root>
		<!-- SETTINGS -->
		<Tooltip.Root>
			<Tooltip.Trigger asChild
			                 let:builder>
				<Button variant="ghost"
				        size="icon"
				        class="rounded-lg aria-[current='page']:bg-muted transition-colors"
				        aria-label="Settings"
				        aria-current="{$page.url.pathname === '/settings' ? 'page' : undefined}"
				        builders={[builder]}
				        href="/settings">
					<Settings2 class="size-5" />
				</Button>
			</Tooltip.Trigger>
			<Tooltip.Content side="right"
			                 sideOffset={5}>Einstellungen
			</Tooltip.Content>
		</Tooltip.Root>
	</nav>
	<nav class="mt-auto grid gap-1 p-2">
		<!-- TEST Nav 2 -->
		<Tooltip.Root>
			<Tooltip.Trigger asChild
			                 let:builder>
				<Button variant="ghost"
				        size="icon"
				        class="mt-auto rounded-lg"
				        aria-label="Account"
				        builders={[builder]}>
					<SquareUser class="size-5" />
				</Button>
			</Tooltip.Trigger>
			<Tooltip.Content side="right"
			                 sideOffset={5}>Account
			</Tooltip.Content>
		</Tooltip.Root>
	</nav>
</aside>
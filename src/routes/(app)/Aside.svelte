<script>
    import * as Tooltip from "$lib/components/ui/tooltip/index.ts";
    import {Button} from "$lib/components/ui/button/index.ts";
    import {Triangle} from "lucide-svelte";
    import {Bot} from "lucide-svelte";
    import {SquareTerminal} from "lucide-svelte";
    import {CodeXml} from "lucide-svelte";
    import {Settings2} from "lucide-svelte";
    import {SquareUser} from "lucide-svelte";
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
		<!-- TEST Nav 1 -->
		<Tooltip.Root>
			<Tooltip.Trigger asChild
			                 let:builder>
				<Button variant="ghost"
				        size="icon"
				        class="rounded-lg bg-muted"
				        aria-label="Playground"
				        builders={[builder]}>

					<SquareTerminal class="size-5" />
				</Button>
			</Tooltip.Trigger>
			<Tooltip.Content side="right"
			                 sideOffset={5}>Playground
			</Tooltip.Content>
		</Tooltip.Root>
		<Tooltip.Root>
			<Tooltip.Trigger asChild
			                 let:builder>
				<Button variant="ghost"
				        size="icon"
				        class="rounded-lg"
				        aria-label="Models"
				        builders={[builder]}>
					<Bot class="size-5" />
				</Button>
			</Tooltip.Trigger>
			<Tooltip.Content side="right"
			                 sideOffset={5}>Models
			</Tooltip.Content>
		</Tooltip.Root>
		<Tooltip.Root>
			<Tooltip.Trigger asChild
			                 let:builder>
				<Button variant="ghost"
				        size="icon"
				        class="rounded-lg"
				        aria-label="API"
				        builders={[builder]}>
					<CodeXml class="size-5" />
				</Button>
			</Tooltip.Trigger>
			<Tooltip.Content side="right"
			                 sideOffset={5}>API
			</Tooltip.Content>
		</Tooltip.Root>
		<Tooltip.Root>
			<Tooltip.Trigger asChild
			                 let:builder>
				<Button variant="ghost"
				        size="icon"
				        class="rounded-lg"
				        aria-label="Settings"
				        builders={[builder]}>
					<Settings2 class="size-5" />
				</Button>
			</Tooltip.Trigger>
			<Tooltip.Content side="right"
			                 sideOffset={5}>Settings
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
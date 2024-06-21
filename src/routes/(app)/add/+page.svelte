<script>
    import "../../styles.css";

    import {Bird, Rabbit, Turtle} from "lucide-svelte";
    import {Badge} from "$lib/components/ui/badge/index.ts";
    import {Label} from "$lib/components/ui/label/index.ts";
    import {Input} from "$lib/components/ui/input/index.ts";

    import * as Select from "$lib/components/ui/select";
</script>

<svelte:head>
	<title>Dashboard</title>
	<meta name="description"
	      content="Svelte demo app" />
</svelte:head>

<main class="grid flex-1 gap-4 overflow-auto p-4 md:grid-cols-2 lg:grid-cols-3">
	<div class="relative hidden flex-col items-start gap-8 md:flex">
		<form class="grid w-full items-start gap-6">
			<fieldset class="grid gap-6 rounded-lg border p-4">
				<legend class="-ml-1 px-1 text-sm font-medium"> Elemente</legend>
				<div class="grid gap-3">
					<Label for="model">Model</Label>
					<Select.Root>
						<Select.Trigger
										id="model"
										class="items-start [&_[data-description]]:hidden">
							<Select.Value placeholder="Select a model" />
						</Select.Trigger>
						<Select.Content>
							<Select.Item value="genesis">
								<div class="flex items-start gap-3 text-muted-foreground">
									<Rabbit class="size-5" />
									<div class="grid gap-0.5">
										<p>
											Neural
											<span class="font-medium text-foreground">
                            Genesis
											</span>
										</p>
										<p class="text-xs"
										   data-description>
											Our fastest model for general use cases.
										</p>
									</div>
								</div>
							</Select.Item>
							<Select.Item value="explorer">
								<div class="flex items-start gap-3 text-muted-foreground">
									<Bird class="size-5" />
									<div class="grid gap-0.5">
										<p>
											Neural
											<span class="font-medium text-foreground">
                            Explorer
											</span>
										</p>
										<p class="text-xs"
										   data-description>
											Performance and speed for efficiency.
										</p>
									</div>
								</div>
							</Select.Item>
							<Select.Item value="quantum">
								<div class="flex items-start gap-3 text-muted-foreground">
									<Turtle class="size-5" />
									<div class="grid gap-0.5">
										<p>
											Neural
											<span class="font-medium text-foreground">
                            Quantum
											</span>
										</p>
										<p class="text-xs"
										   data-description>
											The most powerful model for complex
											computations.
										</p>
									</div>
								</div>
							</Select.Item>
						</Select.Content>
					</Select.Root>
				</div>
				<div class="grid gap-3">
					<Label for="temperature">Temperature</Label>
					<Input id="temperature"
					       type="number"
					       placeholder="0.4" />
				</div>
				<div class="grid grid-cols-2 gap-4">
					<div class="grid gap-3">
						<Label for="top-p">Top P</Label>
						<Input id="top-p"
						       type="number"
						       placeholder="0.7" />
					</div>
					<div class="grid gap-3">
						<Label for="top-k">Top K</Label>
						<Input id="top-k"
						       type="number"
						       placeholder="0.0" />
					</div>
				</div>
			</fieldset>
		</form>
	</div>
	<div class="relative flex h-full flex-col rounded-xl p-4 min-h-[50vh] bg-muted/50 lg:col-span-2">
		<Badge variant="outline"
		       class="absolute top-3 right-3">Vorschau
		</Badge>
		<div class="flex-1"></div>
	</div>
</main>

<style>

</style>

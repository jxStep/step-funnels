<script>
    import Navbar from "./Navbar.svelte";
    import Aside from "./Aside.svelte";
</script>
<div class="grid h-screen w-full  pl-[53px]">
	<div class="flex flex-col">
		<Navbar></Navbar>
		<Aside></Aside>
		<slot></slot>
	</div>
</div>
<script lang="ts">
	import Menu from '@smui/menu';
	import List, { Item, Separator, Text, PrimaryText } from '@smui/list';
	import Button, { Label } from '@smui/button';

	let menu: Menu;
	let anchor: HTMLDivElement;
</script>

<div
	style="width: 100%; height: 48px; display: flex; justify-content: flex-end; align-items: center;"
>
	<Button on:click={() => menu.setOpen(true)} style="margin-right: 16px;">
		<img
			style="width: 24px; height: 24px; background-color:blue; border-radius: 50%;"
			src="/devdata/ganbare_doki_chan.gif"
			alt="profile_img"
		/>
		<div style="margin-left: 8px; font-size: 0.75rem;" bind:this={anchor}>majesnix</div>
	</Button>
	<Menu
		bind:this={menu}
		anchorCorner="BOTTOM_START"
		bind:anchorElement={anchor}
		style="margin-top: 32px; margin-right: 16px;"
	>
		<List>
			<a href="/"><Item><Text>Dashboard</Text></Item></a>
			<a href="/tiles">
				<Item>
					<Text>Tiles</Text>
				</Item>
			</a>
			<Item>
				<Text>Tags</Text>
			</Item>
			<Item>
				<Text>Profile</Text>
			</Item>
			<Item>
				<Text>Users</Text>
			</Item>
			<Item>
				<Text>Settings</Text>
			</Item>
			<Separator />
			<Item>
				<Text>Logout</Text>
			</Item>
		</List>
	</Menu>
</div>

<style>
	a {
		text-decoration: none;
		color: #fff;
	}
</style>

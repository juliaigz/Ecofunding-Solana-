<script>
	import {
		Header,
		HeaderNav,
		HeaderNavItem,
		HeaderUtilities,
		HeaderGlobalAction,
		SideNav,
		SideNavItems,
		SideNavLink,
		SideNavDivider,
		SkipToContent,
		Button
	} from 'carbon-components-svelte';
	import { UserAvatarFilledAlt, SettingsAdjust, Logout } from 'carbon-icons-svelte';
	import WalletConnect from '$lib/walletConnect.svelte';
	import SignIn from './SignIn.svelte';
	import StartACrowfund from './StartACrowfund.svelte';

	let isSideNavOpen = false;
</script>

<Header
	expansionBreakpoint={1700}
	company="Ecofunding"
	platformName="SOL"
	bind:isSideNavOpen
	href="/"
>
	<svelte:fragment slot="skip-to-content">
		<SkipToContent />
	</svelte:fragment>
	<HeaderNav>
		<HeaderNavItem href="/about" text="About" />
		<HeaderNavItem href="/help" text="Help" />
		<HeaderNavItem href="/project" text="Start a project" />
	</HeaderNav>
	<HeaderUtilities>
		<!-- <HeaderGlobalAction iconDescription="Settings" tooltipAlignment="start" icon={SettingsAdjust} /> -->
		<!-- <HeaderGlobalAction iconDescription="Profile" icon={UserAvatarFilledAlt} /> -->
		<!-- <HeaderGlobalAction iconDescription="Log out" tooltipAlignment="end" icon={Logout} /> -->
		<!-- <WalletConnect /> -->
		 <StartACrowfund/>
		 <SignIn/>
	</HeaderUtilities>
</Header>

<SideNav bind:isOpen={isSideNavOpen}>
	<SideNavItems>
		<SideNavLink text="About" />
		<SideNavLink text="Help" />
		<SideNavLink text="Start a project" />
		<SideNavDivider />
	</SideNavItems>
</SideNav>

<style>
</style>

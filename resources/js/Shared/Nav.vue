<template>
    <nav class="ml-6">
        <ul class="flex space-x-3">
            <li>
                <NavLink href="/" :active="$page.component === 'Home'">Home</NavLink>
            </li>
            <li>
                <NavLink href="/users" :active="$page.component.startsWith('Users/')">Users</NavLink>
            </li>
            <li>
                <NavLink href="/settings" :active="$page.component === 'Settings'">Settings</NavLink>
            </li>
            <li>
                <NavLink as="button" method="post" href="/logout">Log Out</NavLink>
            </li>
        </ul>
    </nav>
</template>

<script>
import NavLink from '../Shared/NavLink';

export default {
    components: {  NavLink }
};
</script>
<script lang="ts">
import{drawerStore} from '@skeletonlabs/skeleton';
function drawerClose(): void {
    drawerStore.close();
}
</script>
<nav class="list-nav p-4>">
    <ul>
        <li>
            <a href="/" on:click={drawerClose}>Home</a>
        </li>
        <li>
            <a href="/about" on:click={drawerClose}>About</a>
        </li>
        <li>
            <a href="/sites" on:click={drawerClose}>Sites</a>
        </li>
    </ul>
</nav>
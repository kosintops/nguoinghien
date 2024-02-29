<script>
    import { TreeView, TreeViewItem, RecursiveTreeView } from '@skeletonlabs/skeleton';
</script>

<nav class="text-left p-2 rounded-lg">
    <ul>
        <a href="/"><li class="p-3">Trang chủ</li></a>
        <a href="/about"><li class="p-3">About</li></a>
        <a href="/guide"><li class="p-3">Guide</li></a>
        <a href="/bank"><li class="p-3">TKNH</li></a>
        <li class="p-3">
        <TreeView class="text-left">
        <TreeViewItem>
            Price
            <svelte:fragment slot="children">
                <a href="/price">
                <TreeViewItem>Lưu ý</TreeViewItem>
                </a>
                <TreeViewItem>
                    Project Sekai
                    <svelte:fragment slot="children">
                        <a href="/price/pjsk/jp"><TreeViewItem>
                            Japan
                        </TreeViewItem></a>
                        <a href="/price/pjsk/tw"><TreeViewItem>
                            Taiwan
                        </TreeViewItem></a>
                        <a href="/price/pjsk/kr">
                        <TreeViewItem>
                            Korea
                        </TreeViewItem></a>
                        <a href="/price/pjsk/en"><TreeViewItem>
                            English
                        </TreeViewItem></a>
                    </svelte:fragment>
                </TreeViewItem>
                <a href="/price/d4dj">
                <TreeViewItem>
                    D4DJ (Japan)
                </TreeViewItem>
                </a>
                <a href="/price/mahoyaku">
                <TreeViewItem>
                    Mahoyaku
                </TreeViewItem>
                </a>
            </svelte:fragment>
        </TreeViewItem>
        </TreeView></li>
        <a href="https://jinpots.top"><li class="p-3">Made by JinPots</li></a>
    </ul>
</nav>
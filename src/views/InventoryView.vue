<template>
    <div class="box">
        <p>Coming Soon...</p>
        <!--
        <table>
            <tr>
                <td v-for="tool in tools"><img :src="tool.image" style="height: 50px; width: 50px"></td>
            </tr>
        </table>
    -->
    </div>
</template>

<script>
export default {
    name: 'InventoryView',
    data() {
        return {
            tools:[
                {
                    id: 1,
                    name: "wireshark",
                    image: require("@/assets/icons/icon_wireshark.png")
                },
                {
                    id: 2,
                    name: "sqlmap",
                    image: require("@/assets/icons/icon_sqlmap.jpg")
                },
                {
                    id: 3,
                    name: "bloodhound",
                    image: require("@/assets/icons/icon_bloodhound.png")
                },
                {
                    id: 4,
                    name: "crackmapexec",
                    image: require("@/assets/icons/icon_crackmapexec.jpg")
                }
            ]
        }
    }
}
</script>
<script>

export default {
    name: "AppHeader",
    data() {
        return {
            items: [
                {
                    label: 'characters',
                    url: '#',
                    active: false
                },
                {
                    label: 'comics',
                    url: '#',
                    active: true
                },
                {
                    label: 'movies',
                    url: '#',
                    active: false
                },
                {
                    label: 'tv',
                    url: '#',
                    active: false
                },
                {
                    label: 'games',
                    url: '#',
                    active: false
                },
                {
                    label: 'collectibles',
                    url: '#',
                    active: false
                },
                {
                    label: 'videos',
                    url: '#',
                    active: false
                },
                {
                    label: 'fans',
                    url: '#',
                    active: false
                },
                {
                    label: 'news',
                    url: '#',
                    active: false
                },
                {
                    label: 'shop',
                    url: '#',
                    active: false
                }
            ]
        }
    }
}
</script>
<template lang="">
    <div class="container">
        <div class="row">
            <div class="logo">
                <img class="image-logo" src="../assets/img/dc-logo.png" alt="logo">
            </div>
            <div class="menu-bar">
                <ul>
                    <li v-for="item in items">
                        <a href="#" :class="item.active == true ? 'active' : ''">{{ item.label }}</a>
                    </li>
                </ul>
            </div>
        </div>
        
    </div>
</template>

<style lang="scss">
@use '../styles/partials/variables' as *;

.container {
    width: 100%;
}

.row {
    margin: 0 auto;
    width: 80%;
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: space-between;
}


.image-logo {
    width: 50%;
    margin: 20px 0;
}

.menu-bar {

    li {
        list-style: none;
        display: inline-block;
        margin: 0 0.5rem;
        font-size: 13px;




        a {
            text-transform: uppercase;
            text-decoration: none;
            color: black;
            padding: 36px 0;

            &.active {
                border-bottom: 4px solid;
                border-color: $color_blue;
                color: $color_blue;
            }

            &:hover {
                border-bottom: 4px solid;
                border-color: $color_blue;
                color: $color_blue;
            }
        }
    }
}
</style>
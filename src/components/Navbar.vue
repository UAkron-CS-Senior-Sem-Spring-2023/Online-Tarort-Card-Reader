<template>
            <nav 
            :class="['navbar', 'navbar-expand-lg', 'navbar-dark', 'bg-dark']"
            >
        <div class="container-fluid">
            <a class="navbar-brand" href="#"> Tarot Reading</a>
            <ul class="navbar-nav me-auto mb-2 nb-lg-0">
                <li v-for="(page, index) in pages" class="nav-item" :key="index">
                    <navbar-link
                        :page="page"
                        :isActive="activePage == index"
                        @click.prevent="navLinkClick(index)"
                        >
                    </navbar-link>
                </li>
        </ul>
    </div>
  </nav>   
</template>

<script>
import NavbarLink from './NavbarLink.vue';

export default {
    components: {
        NavbarLink
    },
    props: ['pages', 'activePage', 'navLinkClick' ],

}
</script>
<template>
    <div>
        <nav class="navbar navbar-expand-lg navbar-dark bg-dark shadow-sm">
            <div class="container-fluid">
                <router-link :to="{ name: 'home' }" class="navbar-brand">
                    Laravel-Vue SPA
                </router-link>
                <button
                    class="navbar-toggler"
                    type="button"
                    data-bs-toggle="collapse"
                    data-bs-target="#navbarSupportedContent"
                    aria-controls="navbarSupportedContent"
                    aria-expanded="false"
                    aria-label="Toggle navigation"
                >
                    <span class="navbar-toggler-icon"></span>
                </button>
                <div
                    class="collapse navbar-collapse"
                    id="navbarSupportedContent"
                >
                    <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                        <li class="nav-item">
                            <router-link
                                class="nav-link"
                                data-toggle="collapse"
                                :to="{ name: 'home' }"
                                >Home
                            </router-link>
                        </li>
                        <li class="nav-item">
                            <router-link
                                class="nav-link"
                                data-toggle="collapse"
                                :to="{ name: 'about' }"
                                >About
                            </router-link>
                        </li>
                    </ul>
                </div>
            </div>
        </nav>

        <div class="container">
            <router-view></router-view>
        </div>
    </div>
</template>

<script>
export default {
    watch: {
        $route() {
            $("#navbarSupportedContent").collapse("hide");
        },
    },
};
</script>

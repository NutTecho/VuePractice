<template>
    <div>
        <b-navbar 
            toggleable="lg" 
            type="light" 
            variant="light" 
        >
            <b-navbar-brand href="/">MyWebApp</b-navbar-brand>
            <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
                <b-collapse id="nav-collapse" is-nav>
                    <b-navbar-nav>
                        <b-nav-item href="/about">About</b-nav-item>
                        <b-nav-item href="/cardtest">CardTest</b-nav-item>
                        <b-nav-item href="/charttest">Chart</b-nav-item>
                    </b-navbar-nav>
                </b-collapse>
        </b-navbar>
        <nuxt/>
    </div>
    
</template>



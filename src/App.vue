<script setup></script>

<template>
  <div class="main">
    <div id="header">
        <div class="name">Josh Zak - FullStack Engineer</div>
        <div class="nav">
            <div class="about">About</div>
            <div class="projects">Projects</div>
        </div>
    </div>
    <div class="section1">

    </div>
    <div class="section2">

    </div>
    <div class="section3">

    </div>
    <div class="footer">

    </div>
  </div>
</template>







<style>

*,
*::before,
*::after {
    box-sizing: border-box;
}


.main{
    display: flex;
    flex-direction: column;
}

.main > *{
    border: solid black;
}

#header{
    display: flex;
    justify-content: space-between;
    padding: 0 1rem;
}

.nav{
    display: flex;
    gap: 2rem;
}

</style>

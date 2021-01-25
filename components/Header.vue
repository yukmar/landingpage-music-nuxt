<template>
  <header class="navbar">
    <div class="navbar__nav" title="nav-right">
      <NuxtLink class="navbar__nav-logo" to="/">
        <img src="~/assets/images/logo.png" alt="" />
        <span>Soundwave</span>
      </NuxtLink>
    </div>
    <div class="navbar__nav" title="nav-left">
      <NuxtLink class="navbar__nav-item" to="/discover">Discover</NuxtLink>
      <NuxtLink class="navbar__nav-item" to="/join">Join</NuxtLink>
    </div>
  </header>
</template>

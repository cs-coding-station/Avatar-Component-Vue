<template>
  <div class="mb-10 m-2 flex flex-col justify-center items-center">
    <p>Default</p>
    <Avatar img="woman.jpg" />

    <p>Square</p>
    <Avatar img="woman.jpg" square />

    <p>Border</p>
    <Avatar img="woman.jpg" border />
    <Avatar img="woman.jpg" square border class="mt-2" />

    <p>Icon</p>
    <Avatar />
    <Avatar square class="mt-2" />

    <p>Initials</p>
    <Avatar initials="CS" />
    <Avatar initials="CS" square class="mt-2" />

    <p>Dot</p>
    <Avatar img="woman.jpg" dot />
    <Avatar img="woman.jpg" dot square class="mt-2" />
  </div>
</template>

<script setup></script>

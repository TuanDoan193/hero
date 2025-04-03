<template>
  <div class="admin-layout">
    <aside>
      <ul>
        <li>Dashboard</li>
        <li>User Management</li>
      </ul>
    </aside>
    <main>
      <slot></slot>
    </main>
  </div>
</template>

<style scoped>
.admin-layout {
  display: flex;
}

aside {
  width: 250px;
  background-color: #f4f4f4;
  padding: 20px;
}

main {
  flex: 1;
  padding: 20px;
}
</style>

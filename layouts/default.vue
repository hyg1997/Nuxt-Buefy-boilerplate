<template>
  <div>
    <aside class="sidebar has-background-ftf">
      <div class="user">
        <b-collapse :open="false">
          <span class="user user__username" slot="trigger">
            Username
            <i class="user user__expand-icon material-icons">expand_more</i>
          </span>
          <div>
            <ul class="menu-list">
              <li>
                <a></a>
              </li>
              <li>
                <a>Customers</a>
              </li>
            </ul>
          </div>
        </b-collapse>
      </div>
    </aside>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          title: 'Home',
          icon: 'home',
          to: { name: 'index' }
        },
        {
          title: 'Inspire',
          icon: 'lightbulb',
          to: { name: 'inspire' }
        }
      ]
    }
  }
}
</script>
<style>
:root {
  /* color */
  --bg-color: #1f42c9;
  --color-primary: #ffffff;
  --font-family-primary: 'Fira Sans', sans-serif;

  /* grid */
  --sidebar-width: 19.58vw;
}

.sidebar {
  background-color: var(--bg-color);
  height: 100vh;
  width: var(--sidebar-width);
  padding-left: 3rem;
  padding-top: 3rem;
  color: var(--color-primary);
}

.user__username {
  font-size: 1.75em;
  font-weight: 500;
  font-family: var(--font-family-primary);
}

.user__expand-icon {
  font-size: 1.25em;
  vertical-align: bottom;
  cursor: pointer;
  user-select: none;
}

.menu-list a {
  color: #ffffff;
}
</style>

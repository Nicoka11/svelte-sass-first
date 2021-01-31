<ul class="nav-list">
  <li>Home</li>
  <li>Our Services</li>
  <li>Retail Shops</li>
  <li>About</li>
</ul>

<style lang="scss">
  $main-color: rgb(221, 63, 0);

  .nav-list {
    color: black;
    font-size: 1.5rem;
  }

  li {
    background-color: rgba($color: $main-color, $alpha: 0.1);
    text-transform: uppercase;
    display: inline-block;
    list-style: none;
    padding: 20px;
    border: 2px solid $main-color;
    border-radius: 6px;
    width: 200px;

    &:not(:last-child) {
      margin-right: 5px;
    }
  }
</style>

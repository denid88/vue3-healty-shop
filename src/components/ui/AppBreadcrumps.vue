<template>
  <div class="breadcrumbs_area">
    <div class="container">
      <div class="row">
        <div class="col-12">
          <div class="breadcrumb_content">
            <h3 class="quotes">When <span>diet</span> is correct, <span>medicine</span> is of no need</h3>
            <ul>
              <li>Healty Shop /<router-link to="/">Shop</router-link></li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'AppBreadcrumbs'
}
</script>
<style>
.breadcrumbs_area {
  background-attachment: fixed;
  background-image: url('https://denid88.sirv.com/healthy/banner/1920x200.jpg') !important;
  height: 200px;
}
</style>


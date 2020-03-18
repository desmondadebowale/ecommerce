<template>
    
    <div class="list-group" id="list-tab" role="tablist">
      <a class="list-group-item list-group-item-action active" id="list-home-list" data-toggle="list" href="#list-home" role="tab" aria-controls="home">{{listcategory.name}}</a>
    
    </div>
</template>

<script>
export default {
    props: ["listcategory"]
}
</script>
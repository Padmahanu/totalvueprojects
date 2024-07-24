<template>
    <div class="cards">
<div id="card-header">
<slot name="header"></slot>
</div>
<div id="card-content">
<slot></slot>
</div>
<div id="card-footer">
<slot  name="footer"></slot>
</div>
    </div>
</template>

<script>
    export default {
        name: "Card"
    }
</script>

<style  scoped>
.cards{
    padding: 16px;
    transition: 0.3s;
    margin-bottom: 20px;
    width: 200px;
  box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
}

</style>
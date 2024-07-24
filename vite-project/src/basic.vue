<template>
  <div>
{{name}}
<div v-html="channel"></div>
<div v-html="hack"></div>
<h2 :id="headingId">Heading</h2>
<button :disabled="isDisabled">Bind</button>
<h2 class="underline">Underline text</h2>
<h2 class="underline" :class="status">Status</h2>
<h2 :class="isPromoted && 'promoted'">Movie</h2>
<h2 :class="isSoldout?'new':'old'">Sold out movie</h2>
<h2 :class="['new','promoted']">Newly promoted movie</h2>
<h2 :class="[isSoldout?'new':'old',isPromoted && 'promoted']">Array condition movie</h2>
<h2 :class="{
  promoted : isPromoted,
  new: !isSoldout,
  'sold-out' : true
}">Object condition movie</h2>
<h2 :style="{color: hightcolr,fontSize : headerSize +'px',padding: '20px'}">Inline style</h2>
<h2 :style="[styleadded,twoobjects]">Object style</h2>
  </div>
</template>

<script>
  export default {
    name: "basic",
    data(){
      return {
        name: "padma",
        channel: "<b>padmadev</b>",
        hack: `<a href="#" onClick="alert('You have been hacked')">Win a prize<a/>`,
        headingId: 'heading',
        isDisabled : true,
        status : 'danger',
        isPromoted: true,
        isSoldout: true,
        hightcolr: 'orange',
        headerSize: 50,
        styleadded:{
          fontWeight: 500,
         fontStyle: 'italic'
        },
        twoobjects:{
          color:'pink',
          backgroundColor:'yellow',
          border:'1px solid green'
        }
      };
    }
  }
</script>

<style>
.underline {
  text-decoration: underline;
}
.promoted{
  font-weight: 500;
  font-style: italic;
}
.new{
  color: red;
}
.old{
  color: aqua;
}
</style>
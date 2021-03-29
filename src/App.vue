<template>
 <div id ="app">
<section class="accordion">
    <div class="accordion-container">
      <h4 class="accordiontitle jsAccordionTitle">アコーディオン</h4>
      <div id="overlay" v-if="show">
      <div class="accordioncontent">アコーディオンの中身が入ります</div>
    </div>
    </div>
    </section>
</div>
</template>

<script>
export default {
  data() {
  return {
      show: false
    };
  },
   methods: {
    accordiontitle() {
      this.show = true;
    },
    accordioncontent() {
      this.show = false;
    }
  }
};
</script>


<style>
.accordion{
  margin-top: 10px;
}

.accordion-container {
  width: 500px;
  margin: 0 auto;
}

.accordiontitle {
     position: relative;
    display: block;
    padding: 20px 20px;
    border: 1px solid #E5E5E5;
    border-bottom: none;
    font-size: .875em;
    font-weight: bold;
    cursor: pointer;
    -webkit-transition: .25s;
    transition: .25s;
    background-color: #f6f6f6;
}

.accordioncontent {
  background-color: #e7e7e7;
  padding: 12px 18px;
  margin: 12px 0;
  line-height: normal; /* numberに書き換える*/
  height: auto;
  opacity: 1;
}

</style>


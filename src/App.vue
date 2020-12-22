<template>
  <img style="width: 150px; height: 150px" :src="currentImg" />
  <button @click="makeItTaylor"
          :style="isTaylorClicked ? { 'background-color': '#330ae6' } : null">
    Taylor
  </button>
  <button @click="makeItDemi"
          :style="isDemiClicked ? { 'background-color': '#330ae6' } : null">
    Demi
  </button>
  <button @click="makeItKaty"
          :style="isKatyClicked ? { 'background-color': '#330ae6' } : null">
    Katy
  </button>
</template>

<script>
export default {
  name: 'App',
  data: () => ({
    currentImg: '',
    isTaylorClicked: false,
    isDemiClicked: false,
    isKatyClicked: false,
    taylorImg: 'https://pyxis.nymag.com/v1/imgs/ba2/f85/099d4651e7c4a62bcba5da1fbc5c16be70-18-taylor-swift.rsquare.w1200.jpg',
    katyImg: 'https://upload.wikimedia.org/wikipedia/commons/0/00/Katy_Perry_and_Greg_%2847870635411%29_%28cropped%29.jpg',
    demiImg: 'https://media.npr.org/assets/img/2017/09/28/demi_lovato_03_017_sq-0bf7c082a68df5ddab4e31b04c097d5aa0656e47-s1000.jpg',
  }),
  methods: {
    makeItTaylor() {
      this.currentImg = this.taylorImg
      this.isTaylorClicked = true
      this.isDemiClicked = false
      this.isKatyClicked = false
    },
    makeItKaty() {
      this.currentImg = this.katyImg
      this.isKatyClicked = true
      this.isDemiClicked = false
      this.isTaylorClicked = false
    },
    makeItDemi() {
      this.currentImg = this.demiImg
      this.isDemiClicked = true
      this.isKatyClicked = false
      this.isTaylorClicked = false
    }
  },
  beforeMount() {
    this.makeItTaylor()
  }
}
</script>

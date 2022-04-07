<template>
  <div>
    {{ `Fabric Test` }}
    <canvas id="canvas" width="1200" height="800"></canvas>
  </div>
</template>
<script>
import { fabric } from "fabric";
export default {
  data() {
    return {
      canvasObject: {},
    };
  },
  mounted() {
    this.canvasObject = new fabric.Canvas(document.getElementById("canvas"));
    this.addImage();
  },
  methods: {
    addImage() {
      let _this = this;
      let url =
        "https://th.bing.com/th/id/R.864f96ffdd6dc50743d984c9250a7410?rik=tNMMSF0DwnvTZA&riu=http%3a%2f%2fwww.jyhome.com%2fuploadfiles%2fimages%2f2018%2f3%2f20180330022030400.jpg&ehk=eS%2fRs2cFEMpax9TuDOEYKc3FRUK4or7mFsBKDHgtrbU%3d&risl=&pid=ImgRaw&r=0";
      // "https://cdn.artboard.studio/private/5cb9c751-5f17-4062-adb7-6ec2c137a65d/user_uploads/5bafe170-1580-4d6b-a3be-f5cdce22d17d-asdasdasd.jpg";
      // "https://www.antony-tech.com/resources/materials/origin/60ed4d1ab29be326369c7636.png";
      fabric.Image.fromURL(
        url,
        function (oImg) {
          oImg.set({
            left: 0,
            top: 0,
            scaleX: 0.3,
            scaleY: 0.3,
            originX: "center",
            originY: "center",
            productType: "Product",
            productId: "xxxxxx",
          });
          _this.canvasObject.add(oImg);
        },
        { crossOrigin: "anonymous" }
      );
    },
  },
};
</script>
<style scoped>
</style>
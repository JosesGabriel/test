<template>
  <section class="flex">
    <div class="canvas" ref="container"></div>
    <div class="flex text canvas__text">
      <div>Hello, I'm Joses.</div>
      Software Engineer & Educator.
    </div>
  </section>
</template>

<script>
import * as THREE from "three";
export default {
  data() {
    return {
      camera: null,
      scene: null,
      renderer: null,
      mesh: null,
      stars: null,
      starsGeo: null,
      starImg: require("../assets/star.png"),
    };
  },
  mounted() {
    this.initialize();
  },
  methods: {
    initialize() {
      let container = this.$refs["container"];
      this.scene = new THREE.Scene();
      this.scene.background = new THREE.Color(0x0c1821);
      this.camera = new THREE.PerspectiveCamera(
        60,
        window.innerWidth / window.innerHeight,
        1,
        1000
      );
      this.camera.position.z = 1;
      this.camera.rotation.x = Math.PI / 2;

      this.renderer = new THREE.WebGLRenderer();
      this.renderer.setSize(window.innerWidth, window.innerHeight);
      container.append(this.renderer.domElement);

      this.starGeo = new THREE.Geometry();
      for (let i = 0; i < 3000; i++) {
        let star = new THREE.Vector3(
          Math.random() * 600 - 300,
          Math.random() * 600 - 300,
          Math.random() * 600 - 300
        );

        star.velocity = 0;
        star.acceleration = 0.002;
        this.starGeo.vertices.push(star);
      }

      let sprite = new THREE.TextureLoader().load(this.starImg);
      let starMaterial = new THREE.PointsMaterial({
        color: 0xffffff,
        size: 0.7,
        map: sprite,
      });

      this.stars = new THREE.Points(this.starGeo, starMaterial);
      this.scene.add(this.stars);

      window.addEventListener("resize", this.onWindowResize, false);

      this.animate();
    },
    onWindowResize() {
      this.camera.aspect = window.innerWidth / window.innerHeight;
      this.camera.updateProjectionMatrix();
      this.renderer.setSize(window.innerWidth, window.innerHeight);
    },
    animate: function () {
      this.starGeo.vertices.forEach((p) => {
        p.velocity += p.acceleration;
        p.x -= p.velocity;
        if (p.x < -300) {
          p.x = window.innerWidth / 5;
          p.velocity = 0;
        }
      });
      this.starGeo.verticesNeedUpdate = true;
      this.renderer.render(this.scene, this.camera);
      requestAnimationFrame(this.animate);
    },
  },
};
</script>

<style scoped>
.text {
  color: white;
  font-size: 1.5rem;
}
.canvas {
  height: 100%;
  left: 0;
  position: absolute;
  top: 0;
  width: 100vw;
  z-index: -1;
}
.canvas__text {
  height: 100vh;
}
</style>

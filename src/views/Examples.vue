<template>
  <div class="example">
    <ul>
      <li>
        <pre>pl 154,35 170,130 110,203</pre>
        <pre>p 200,10 250,190 160,210</pre>
        <pre>c 20 100 20</pre>
        <pre>r 100 50 25 25</pre>
        <pre>r 50 150 50 25</pre>
      </li>
      <li>
        <h3>
          --- or ---
        </h3>
        <pre>pl      154   ,35         170,  130  110  ,  203 </pre>
        <pre>p   200  ,10                250,  190 160 , 210 </pre>
        <pre></pre>
        <pre>c          20  100  20</pre>
        <pre>r 100   50            25  25  </pre>
        <pre>R  50 150  50 25  </pre>
      </li>
    </ul>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.example ul li h2 {
  font-size: 30px;
  margin: 0;
  padding-bottom: 5px;
}
.example ul {
  padding: 0;
}
.example ul li pre {
  font-size: 16px;
}
.example ul li {
  list-style-type: none;
}
.example {
  overflow: auto;

  width: 450px;
  height: 500px;

  background: rgb(240, 246, 246);
  border-radius: 10%;

  margin: 40px auto;

  padding: 15px;
  padding-bottom: 2px;
  padding-right: 10px;
  border-bottom-left-radius: 18px;
  border-bottom-right-radius: 18px;
  background-color: rgb(228, 245, 242);

  display: flex;
  flex-direction: column;
  justify-content: center;
}
</style>

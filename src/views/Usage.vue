<template>
  <div class="usage">
    <ul>
      <li>
        <h2>
          Draw circle
        </h2>
        <pre>c &lt;CX Coordinate&gt; &lt;CY Coordinate&gt; &lt;Radius&gt;</pre>
        <pre>C &lt;CX Coordinate&gt; &lt;CY Coordinate&gt; &lt;Radius&gt;</pre>
      </li>
      <li>
        <h2>
          Draw rectangle
        </h2>
        <pre>r &lt;X Coordinate&gt; &lt;Y Coordinate&gt; &lt;Width&gt; &lt;Height&gt;</pre>
        <pre>R &lt;X Coordinate&gt; &lt;Y Coordinate&gt; &lt;Width&gt; &lt;Height&gt;</pre>
      </li>
      <li>
        <h2>
          Draw polygon
        </h2>
        <pre>p &lt;X1,Y1&gt; &lt;X2,Y2&gt; ... &lt;Xn,Yn&gt;</pre>
        <pre>P &lt;X1,Y1&gt; &lt;X2,Y2&gt; ... &lt;Xn,Yn&gt;</pre>
      </li>
      </li>
      <li>
        <h2>
          Draw polyline
        </h2>
        <pre>pl &lt;X1,Y1&gt; &lt;X2,Y2&gt; ... &lt;Xn,Yn&gt;</pre>
        <pre>PL &lt;X1,Y1&gt; &lt;X2,Y2&gt; ... &lt;Xn,Yn&gt;</pre>
      </li>
    </ul>
  </div>
</template>

<style scoped>
.usage ul li h2 {
  font-size: 30px;
  margin: 0;
  padding-bottom: 5px;
}
.usage ul {
  padding-top: 30px;
}
.usage ul li pre {
  font-size: 15px;
}
.usage ul li {
  list-style-type: none;
  padding-top: 15px;
}
.usage {
  overflow: auto;

  width: 450px;
  height: 500px;

  background: rgb(240, 246, 246);
  border-radius: 10%;
  border-top-right-radius: 0%;

  margin: 40px auto;

  display: flex;
  flex-direction: column;
  justify-content: center;

  padding: 15px;
  padding-bottom: 2px;
  padding-right: 10px;
  border-bottom-left-radius: 18px;
  border-bottom-right-radius: 18px;
  background-color: rgb(228, 245, 242);
}
</style>

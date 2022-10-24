<template>
  <div id="container">
    <div id="title-container">
      <h1>Roadmap</h1>
      <p>By Isaac N.C. Visit website</p>
    </div>
    <div id="task-container">
      <div>
        <h2>Backlog</h2>
      </div>
      <div>
        <h2>To do</h2>
      </div>
      <div>
        <h2>In progress</h2>
      </div>
      <div>
        <h2>Designed</h2>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "TodoPage",
};
</script>

<style scoped>
#container {
  display: flex;
  flex-direction: column;
  margin-inline: auto;
  width: calc((368px * 4) + (10px * 3));
}

#title-container {
  display: flex;
  flex-direction: column;
  gap: 10px;
  width: 200px;
  margin-bottom: 50px;
  color: white;
}

#title-container > h1 {
  font-family: 'SF-Pro-Display';
}

#title-container > p {
  margin: 0;
}

#task-container {
  display: flex;
  justify-content: center;
  gap: 24px;
  background-color: grey;
}

#task-container > div {
  width: 368px;
  background-color: #262626;
}
</style>

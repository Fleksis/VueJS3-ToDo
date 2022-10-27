<template>
  <div id="container">
    <div id="title-container">
      <h1>Roadmap</h1>
      <p>By Isaac N.C. Visit website</p>
    </div>
    <div id="task-container">
      <div>
        <p>Backlog</p>
        <TaskComponent
          title="Twilio integration"
          description="Create new note via SMS. Support text, audio, links, and media."
          color="#C440A1"
        />
        <TaskComponent
          title="Markdown support"
          description="Markdown shorthand converts to formatting"
          color="#7678D1"
          label="Formatting"
        />
      </div>
      <div>
        <p>To do</p>
        <TaskComponent title="Tablet view" description="" color="#D93535" />
        <TaskComponent
          title="Audio recording in note"
          description="Show audio in a note and playback UI"
          color="#6A6DCD"
          label="Note interface"
        />
        <TaskComponent
          title="Bookmark in note"
          description="Show rich link UI in a note, and feature to render website screenshot."
          color="#6A6DCD"
          label="Note interface"
        />
        <TaskComponent
          title="Image viewer"
          description="Opens when clicking on the thumbnail in the list or on the image in the note"
          color="#6A6DCD"
        />
      </div>
      <div>
        <p>In progress</p>
        <TaskComponent
          title="Mobile view"
          description="Functions for both web responsive and native apps. Note: Android and iOS will need unique share icons."
          color="#DA3A3A"
        />
        <TaskComponent
          title="Desktop view"
          description="PWA for website and native apps. Note: Windows and Mac will need unique share icons."
          color="#DA3A3A"
        />
        <TaskComponent
          title="Formatting options"
          description="Mobile formatting bar expands and collapses when tapping the format icon."
          color="#3F88E4"
        />
        <TaskComponent
          title="Media in note"
          description="Image & video with player UI"
          color="#7678D1"
          label="Note interface"
        />
      </div>
      <div>
        <p>Designed</p>
        <TaskComponent
          title="Audio recording"
          description="Interface for when recording a new audio note"
          color="#00B294"
          label="New note"
        />
        <TaskComponent
          title="Bookmarking"
          description="Interface for when creating a new link note."
          color="#00B294"
          label="New note"
        />
        <TaskComponent
          title="Mobile home screen"
          description="Folders, tags, and notes lists are sorted by recent."
          color="#3F88E4"
        />
      </div>
    </div>
  </div>
</template>

<script>
import TaskComponent from "@/components/Task.vue";
export default {
  name: "TodoPage",
  components: { TaskComponent },
};
</script>

<style scoped>
#container {
  display: flex;
  flex-direction: column;
  margin-inline: auto;
  gap: 25px;
  width: fit-content;
}

#title-container {
  display: flex;
  flex-direction: column;
  gap: 5px;
  padding: 24px;
  width: 200px;
  color: white;
}

#title-container > h1 {
  font-size: 50px;
  margin-block: 10px;
  font-family: "SF-Pro-Display-Bold";
}

#title-container > p {
  margin: 0;
  text-decoration: underline;
  font-family: "SF-Pro-Display-Regular";
}

#task-container {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  align-items: flex-start;
  gap: 24px;
}

#task-container > div {
  display: flex;
  flex-direction: column;
  width: 344px;
  padding: 24px;
  background-color: #262626;
  border-radius: 16px;
  gap: 24px;
}

#task-container > div > p {
  margin: 0;
  font-size: 37px;
  color: white;
  font-family: "SF-Pro-Display-Bold";
}
</style>

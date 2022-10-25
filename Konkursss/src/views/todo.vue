<template>
  <div id="container">
    <div id="title-container">
      <h1>Roadmap</h1>
      <p>By Isaac N.C. Visit website</p>
    </div>
    <div id="task-container">
      <div>
        <p>Backlog</p>
        <draggable v-model="backlog" group="tasks" @start="drag = true" @end="drag = false" item-key="id">
          <template #item="{ element }">
            <TaskComponent :title="element.title" :description="element.description" :color="element.color" :label="element.label"/>
          </template>
        </draggable>
      </div>
      <div>
        <p>To do</p>
        <draggable v-model="todo" group="tasks" @start="drag = true" @end="drag = false" item-key="id">
          <template #item="{ element }">
            <TaskComponent :title="element.title" :description="element.description" :color="element.color" :label="element.label"/>
          </template>
        </draggable>
      </div>
      <div>
        <p>In progress</p>
        <draggable v-model="inProgress" group="tasks" @start="drag = true" @end="drag = false" item-key="id">
          <template #item="{ element }">
            <TaskComponent :title="element.title" :description="element.description" :color="element.color" :label="element.label"/>
          </template>
        </draggable>
      </div>
      <div>
        <p>Designed</p>
        <draggable v-model="designed" group="tasks" @start="drag = true" @end="drag = false" item-key="id">
          <template #item="{ element }">
            <TaskComponent :title="element.title" :description="element.description" :color="element.color" :label="element.label" />
          </template>
        </draggable>
      </div>
    </div>
  </div>
</template>

<script>
import draggable from "vuedraggable";
import TaskComponent from "@/components/Task.vue";
export default {
  name: "TodoPage",
  components: {
    TaskComponent,
    draggable,
  },
  data() {
    return {
      backlog: [
        {
          id: 1,
          title: "Twilio integration",
          description: "Create new note via SMS. Support text, audio, links, and media.",
          color: "#C94AA8",
          label: "",
        },
        {
          id: 2,
          title: "Markdown support",
          description: "Markdown shorthand converts to formatting",
          color: "#7678D1",
          label: "Formatting",
        },
      ],
      todo: [
        {
          id: 1,
          title: "Tablet view",
          description: "",
          color: "#D93535",
          label: "",
        },
        {
          id: 2,
          title: "Audio recording in note",
          description: "Show audio in a note and playback UI",
          color: "#6A6DCD",
          label: "Note interface",
        },
        {
          id: 3,
          title: "Bookmark in note",
          description: "Show rich link UI in a note, and feature to render website screenshot.",
          color: "#6A6DCD",
          label: "Note interface",
        },
        {
          id: 4,
          title: "Image viewer",
          description: "Opens when clicking on the thumbnail in the list or on the image in the note",
          color: "#6A6DCD",
          label: "",
        },
      ],
      inProgress: [
        {
          id: 1,
          title: "Mobile view",
          description: "Functions for both web responsive and native apps. Note: Android and iOS will need unique share icons.",
          color: "#DA3A3A",
          label: "",
        },
        {
          id: 2,
          title: "Desktop view",
          description: "PWA for website and native apps. Note: Windows and Mac will need unique share icons.",
          color: "#DA3A3A",
          label: "",
        },
        {
          id: 3,
          title: "Formatting options",
          description: "Mobile formatting bar expands and collapses when tapping the format icon.",
          color: "#3F88E4",
          label: "",
        },
        {
          id: 4,
          title: "Media in note",
          description: "Image & video with player UI",
          color: "#7678D1",
          label: "Note interface",
        },
      ],
      designed: [
        {
          id: 1,
          title: "Audio recording",
          description: "Interface for when recording a new audio note",
          color: "#00B294",
          label: "New note",
        },
        {
          id: 2,
          title: "Bookmarking",
          description: "Interface for when creating a new link note.",
          color: "#00B294",
          label: "New note",
        },
        {
          id: 3,
          title: "Mobile home screen",
          description: "Folders, tags, and notes lists are sorted by recent.",
          color: "#3F88E4",
          label: "",
        },
      ],
      drag: false,
    };
  },
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

#task-container > div > div {
  display: flex;
  flex-direction: column;
  gap: 24px;
}

#task-container > div > p {
  margin: 0;
  font-size: 37px;
  color: white;
  font-family: "SF-Pro-Display-Bold";
}
</style>

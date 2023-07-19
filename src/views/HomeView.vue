<template>
  <div class="data">
    <div class="data-element" v-for="el in structure">
      <span class="name-data-element">Name: {{ el.name }}</span>
      <span class="value-data-element">Value: {{ el.value }}</span>
      <span class="edit-data-element" @click="openEditWindow(el.name, el.value)">Edit</span>
    </div>
  </div>
  <EditWindow ref="EditWindow" @confirm="onConfirm" />
</template>

<script>
import EditWindow from '../components/EditWindow.vue';
export default {
    name: "Home",
    methods: {
      openEditWindow(name, value) {
        this.$refs.EditWindow.dialogVisible = true
        this.$refs.EditWindow.name = name
        this.$refs.EditWindow.value = value
      },
      onConfirm(data) {
        let elementToChange = this.structure.find(el => el.name === data.name)
        elementToChange.value = data.value
      }
    },
    data() {
        return {
            dialogVisible: false,
            structure: [
                {
                    "name": "foo1",
                    "value": "bar1"
                },
                {
                    "name": "foo2",
                    "value": "bar2"
                },
                {
                    "name": "foo3",
                    "value": "bar3"
                },
                {
                    "name": "foo4",
                    "value": "bar4"
                },
                {
                    "name": "foo5",
                    "value": "bar5"
                },
                {
                    "name": "foo6",
                    "value": "bar6"
                },
                {
                    "name": "foo7",
                    "value": "bar7"
                },
                {
                    "name": "foo8",
                    "value": "bar8"
                },
                {
                    "name": "foo9",
                    "value": "bar9"
                },
                {
                    "name": "foo10",
                    "value": "bar10"
                },
                {
                    "name": "foo11",
                    "value": "bar11"
                },
                {
                    "name": "foo12",
                    "value": "bar12"
                },
                {
                    "name": "foo13",
                    "value": "bar13"
                },
                {
                    "name": "foo14",
                    "value": "bar14"
                },
                {
                    "name": "foo15",
                    "value": "bar15"
                },
                {
                    "name": "foo16",
                    "value": "bar16"
                },
                {
                    "name": "foo17",
                    "value": "bar17"
                },
                {
                    "name": "foo18",
                    "value": "bar18"
                },
                {
                    "name": "foo19",
                    "value": "bar19"
                },
                {
                    "name": "foo20",
                    "value": "bar20"
                },
                {
                    "name": "foo21",
                    "value": "bar21"
                },
                {
                    "name": "foo22",
                    "value": "bar22"
                },
                {
                    "name": "foo23",
                    "value": "bar23"
                },
                {
                    "name": "foo24",
                    "value": "bar24"
                },
                {
                    "name": "foo25",
                    "value": "bar25"
                },
                {
                    "name": "foo26",
                    "value": "bar26"
                },
                {
                    "name": "foo27",
                    "value": "bar27"
                },
                {
                    "name": "foo28",
                    "value": "bar28"
                },
                {
                    "name": "foo29",
                    "value": "bar29"
                },
                {
                    "name": "foo30",
                    "value": "bar30"
                }
            ]
        };
    },
    components: { EditWindow }
}
</script>

<style lang="scss">
.data {
  margin: 0 auto;
  width: 300px;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 10px;

  .data-element {
    width: 100%;
    background-color: aliceblue;
    padding: 5px;
    display: flex;
    justify-content: space-between;
    border-bottom: 1px solid rgb(162, 162, 162);
    margin-bottom: 10px;
    box-shadow: 0 5px 5px rgba(0.1, 0.1, 0.1, 0.3);

    .name-data-element {
      width: 100px;
      margin-right: 20px;
    }

    .value-data-element {
      width: 100px;
    }

    .edit-data-element {
      margin-left: auto;
      cursor: pointer;
    }
  }
}
</style>

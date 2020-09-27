<template>
  <div>
    <div class="flex content-between flex-wrap bg-gray-800">
      <div class="w-1/3 p-2"></div>
      <div class="w-1/3 p-2 flex items-center">
        <div class="w-full rounded overflow-hidden shadow-lg">
          <div class="px-0 py-0">
            <div class="card-header px-5 py-1">
              <div class="font-bold text-xl mb-2">
                <h6><span>Estado</span></h6>
              </div>
            </div>
            <div class="card-body">
              <Mentionable :keys="['@']" :items="items" offset="6">
                <textarea v-model="text" rows="5" class="text-white p-2" />
              </Mentionable>
            </div>

            <div class="relative bg-gray-800 p-2 text-right">
              <span class="discard">Discard</span>

              <button
                class="bg-purple-700 hover:bg-purple-600 text-sm text-white font-bold py-1 px-2 border border-blue-700 rounded"
              >
                Publicar
              </button>
            </div>
          </div>
        </div>
      </div>
      <div class="w-1/3 p-2 clear-both"></div>
    </div>
  </div>
</template>

<script>
import { Mentionable } from "vue-mention";
export default {
  components: {
    Mentionable,
  },
  data() {
    return {
      text: "",
      items: [
        {
          value: 1234567890,
          label: "Mariano_Miguel",
          image:
            "https://i.pinimg.com/originals/09/65/72/0965721404d9278f1abe136620c9d3a4.jpg",
        },
        {
          value: 1234567891,
          label: "MariCel",
          image:
            "https://pm1.narvii.com/6894/1b46328498c7fcf0bd16f68d9956490d95e415f7r1-256-256v2_00.jpg",
        },
        {
          value: 1234567892,
          label: "Inserte.nombre",
          image:
            "https://media.tenor.com/images/52373c8b4b03cbd4edd736f8782aea06/tenor.png",
        },
        {
          value: 1234567893,
          label: "Mariano_Miguel02",
          image:
            "https://images.vexels.com/media/users/3/149881/isolated/lists/010ff490d872217def55fe541540e9f9-ilustracion-de-anime-inocente.png",
        },
      ],
    };
  },
};
</script>

<style>
.mention-item {
  padding: 4px 4px;
  border-radius: 4px;
  color: azure;
}

.mention-selected {
  background: rgb(192, 250, 153);
  color: #21283b;
}

.discard {
  color: aliceblue;
  font-size: 14px;
  margin-right: 10px;
}
.card-footer {
  background: #1d2333;
  border-color: #21283b;
  padding: 5px;
}
.card-header {
  background: #1d2333;
  color: aliceblue;
  border-color: #21283b;
}
textarea {
  width: 100%;
  background: #21283b;
  color: azure;
  padding: 10px;
  border-color: #21283b;
}
textarea:focus {
  outline: none !important;
  border-color: #21283b;
  box-shadow: 0 0 10px #1d2333;
  color: azure;
  padding: 10px;
}
h6 span {
  border-bottom: 2px solid #4ff461;
  padding-bottom: 10px;
}
.card-body {
  padding: 0px !important;
  margin-bottom: -6px;
}
body {
  background-color: #2d3748 !important;
}
</style>
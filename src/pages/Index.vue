<template>
  <q-page class="q-pa-md">
    <div class="row q-col-gutter-sm">
      <div class="col-5">
        <q-card dark bordered class="bg-grey-9">
          <q-card-section class="row">
            <q-card class="col q-mr-sm my-card-1" dark>
              <q-card-section>
                <div class="text-h5 text-center">Living Room Temprature</div>
                <div class="text-h5 text-center">20 &#8451;</div>
                <div class="row justify-center">
                  <q-knob
                    :min="5"
                    :max="40"
                    v-model="value1"
                    show-value
                    size="90px"
                    :thickness="0.22"
                    color="teal"
                    track-color="grey-3"
                    class="q-ma-md"
                  />
                </div>
                <div class="row">
                  <trend
                    :data="[0, 2, 5, 9, 5, 10, 3, 5, 0, 0, 1, 8, 2, 9, 0]"
                    :gradient="['#6fa8dc', '#42b983', '#2c3e50']"
                    auto-draw
                    smooth
                  ></trend>
                </div>
              </q-card-section>
            </q-card>
            <q-card class="col my-card-1" dark>
              <q-card-section>
                <div class="text-h5 text-center">Bed Room 1</div>
                <div class="text-h5 text-center">20 &#8451;</div>
                <div class="row justify-center">
                  <q-knob
                    :min="5"
                    :max="40"
                    v-model="value1"
                    show-value
                    size="90px"
                    :thickness="0.22"
                    color="teal"
                    track-color="grey-3"
                    class="q-ma-md"
                  />
                </div>
                <div class="row">
                  <trend
                    :data="[0, 2, 5, 9, 5, 1, 6, 5, 0, 2, 1, 4, 2, 9, 0]"
                    :gradient="['#6fa8dc', '#42b983', '#2c3e50']"
                    auto-draw
                    smooth
                  ></trend>
                </div>
              </q-card-section>
            </q-card>
          </q-card-section>
          <q-card-section class="row justify-between">
            <q-card class="col q-mr-sm" dark>
              <q-card-section>
                <div class="text-h5 text-center">Bed Room 2</div>
                <div class="text-h5 text-center">{{value1}} &#8451;</div>
                <div class="row justify-center">
                  <q-knob
                    :min="5"
                    :max="40"
                    v-model="value1"
                    show-value
                    size="90px"
                    :thickness="0.22"
                    color="teal"
                    track-color="grey-3"
                    class="q-ma-md"
                  />
                </div>
                <div class="row">
                  <trend
                    :data="[0, 2, 4, 2, 6, 1, 0, 5, 1, 6, 1, 4, 2, 9, 0]"
                    :gradient="['#6fa8dc', '#42b983', '#2c3e50']"
                    auto-draw
                    smooth
                  ></trend>
                </div>
              </q-card-section>
            </q-card>
            <q-card class="col q-mr-sm" dark>
              <q-card-section>
                <div class="text-h5 text-center">Study Room</div>
                <div class="text-h5 text-center">{{value1}} &#8451;</div>
                <div class="row justify-center">
                  <q-knob
                    :min="5"
                    :max="40"
                    v-model="value1"
                    show-value
                    size="90px"
                    :thickness="0.22"
                    color="teal"
                    track-color="grey-3"
                    class="q-ma-md"
                  />
                </div>
                <div class="row">
                  <trend
                    :data="[0, 2, 5, 9, 4, 1, 1, 3, 0, 2, 1, 4, 2, 9, 0]"
                    :gradient="['#6fa8dc', '#42b983', '#2c3e50']"
                    auto-draw
                    smooth
                  ></trend>
                </div>
              </q-card-section>
            </q-card>
            <q-card class="col q-mr-sm" dark>
              <q-card-section>
                <div class="text-h5 text-center">Office Room</div>
                <div class="text-h5 text-center">{{value1}} &#8451;</div>
                <div class="row justify-center">
                  <q-knob
                    :min="5"
                    :max="40"
                    v-model="value1"
                    show-value
                    size="90px"
                    :thickness="0.22"
                    color="teal"
                    track-color="grey-3"
                    class="q-ma-md"
                  />
                </div>
                <div class="row">
                  <trend
                    :data="[0, 2, 5, 9, 4, 1, 1, 3, 0, 2, 1, 4, 2, 9, 0]"
                    :gradient="['#6fa8dc', '#42b983', '#2c3e50']"
                    auto-draw
                    smooth
                  ></trend>
                </div>
              </q-card-section>
            </q-card>
          </q-card-section>
        </q-card>
      </div>
      <div class="col-7">
        <q-card dark bordered class="bg-grey-9">
          <q-card-section class="row">
            <q-card class="col q-mr-sm" dark>
              <q-card-section>
                <div class="row justify-center">
                  <p>Living Room</p>
                </div>
                <div class="row justify-center">
                  <i
                    :class="[bulb1? 'fas fa-lightbulb fa-3x text-yellow glowinganim':'fas fa-lightbulb fa-3x text-white']"
                  ></i>
                </div>
                <q-toggle color="yellow" v-model="bulb1" />
              </q-card-section>
            </q-card>
            <q-card class="col q-mr-sm" dark>
              <q-card-section>
                <div class="row justify-center">
                  <p>Living Room</p>
                </div>
                <div class="row justify-center">
                  <i
                    :class="[bulb2? 'fas fa-lightbulb fa-3x text-yellow glowinganim':'fas fa-lightbulb fa-3x text-white']"
                  ></i>
                </div>
                <q-toggle color="yellow" v-model="bulb2" />
              </q-card-section>
            </q-card>
            <q-card class="col q-mr-sm" dark>
              <q-card-section>
                <div class="row justify-center">
                  <p>Living Room</p>
                </div>
                <div class="row justify-center">
                  <i
                    :class="[bulb3? 'fas fa-lightbulb fa-3x text-yellow glowinganim':'fas fa-lightbulb fa-3x text-white']"
                  ></i>
                </div>
                <q-toggle color="yellow" v-model="bulb3" />
              </q-card-section>
            </q-card>
            <q-card class="col q-mr-sm" dark>
              <q-card-section>
                <div class="row justify-center">
                  <p>Living Room</p>
                </div>
                <div class="row justify-center">
                  <i
                    :class="[bulb4? 'fas fa-lightbulb fa-3x text-yellow glowinganim':'fas fa-lightbulb fa-3x text-white']"
                  ></i>
                </div>
                <q-toggle color="yellow" v-model="bulb4" />
              </q-card-section>
            </q-card>
          </q-card-section>
          <q-card-section class="row justify-between">
            <q-card class="col q-mr-sm" dark>
               <q-card-section>
                <div class="row justify-center">
                  <p>NOW</p>
                </div>
                <div class="row justify-center">
                  
                </div>
                
              </q-card-section>
            </q-card>
            <q-card class="col q-mr-sm" dark>
              <q-card-section>
                <div class="text-h5 text-center">Bed Room 1</div>
                <div class="text-h5 text-center">{{value1}} &#8451;</div>
                <div class="row justify-center">
                  <q-knob
                    :min="5"
                    :max="40"
                    v-model="value1"
                    show-value
                    size="90px"
                    :thickness="0.22"
                    color="teal"
                    track-color="grey-3"
                    class="q-ma-md"
                  />
                </div>
              </q-card-section>
            </q-card>
            <q-card class="col q-mr-sm" dark>
              <q-card-section>
                <div class="text-h5 text-center">Bed Room 1</div>
                <div class="text-h5 text-center">{{value1}} &#8451;</div>
                <div class="row justify-center">
                  <q-knob
                    :min="5"
                    :max="40"
                    v-model="value1"
                    show-value
                    size="90px"
                    :thickness="0.22"
                    color="teal"
                    track-color="grey-3"
                    class="q-ma-md"
                  />
                </div>
              </q-card-section>
            </q-card>
          </q-card-section>
        </q-card>
      </div>
    </div>
  </q-page>
</template>

<script>
import Vue from "vue";
import Trend from "vuetrend";
Vue.use(Trend);
export default {
  name: "PageIndex",
  data() {
    return {
      url: "asd",
      history: {},
      search_query: "q=rich_dad poor dada",
      value1: 20,
      bulb1: false,
      bulb2: false,
      bulb3: false,
      bulb4: false
    };
  },
  methods: {
    getHistoryData() {
      console.log("calling hook");
      this.$q.bex.send("test").then(r => {
        console.log("Text has been highlighted");
        console.log(r);
      });
    },
    getBookData() {
      this.$axios
        .get(
          'https://www.googleapis.com/books/v1/volumes?q="rich dad"&'
        )
        .then(function(res) {
          console.log(res);
        });
    }
  },
  mounted() {
    console.log("I a mounrted");
  },
  created() {
    console.log("created");
    // this.getHistoryData()
  },
  beforeDestroy() {}
};
</script>
<style >
.my-card-1 {
  width: 150px;
}
.my-card-2 {
  width: 100%;
  max-width: 350px;
  height: 250px;
}
.glowinganim {
  animation: glowing 1300ms infinite;
}
@keyframes glowing {
  /* 0% { color: #CCCC00; } */
  50% {
    color: #e4d00a;
  }
  100% {
    color: #fff700;
  }
}
</style>
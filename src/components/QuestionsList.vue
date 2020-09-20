<template>
  <div class="container-fluid dashboard">
    <div class="row">
      <div class="col">
        <div class="row">
          <div class="col-sm">
            <div class="card" id="qoutes">
              <div class="card-body">
                <div class="media align-items-center">
                  <div class="media-body">
                    <span>"Your time is limited, so don't waste it living someone else's life." <br> "Thời gian của bạn luôn có hạn, vì vậy đừng lãng phí nó để sống cuộc đời khác."</span>
                    </div>
                        <div class="text-center">
                            <i class="icofont-education"></i>
                        </div>
                    </div>
                  </div>
              </div>
          </div>

          <div class="col-sm">
            <div class="card search">
                <center>
                  <h4 id="title">Questions and Answers</h4>
                  <b-container class="bv-example-row">
                    <b-row>
                      <b-col class="col-8"><b-form-input v-model="keyword" type="text" debounce="500" placeholder="Search Question" id="keyword-input"></b-form-input></b-col>
                      <b-col class="col-4"><b-button>Search</b-button></b-col>
                    </b-row>
                  </b-container>
                </center>
            </div>
          </div> 
        </div>

        <div class="card question-list">
          <div class="title-card">
            <h4>Question List</h4>
          </div>
            <div class="questionList">
              <table v-if="items.length" class="table table-hover">
                <thead>
                  <tr>
                    <th>#</th>
                    <th class="pick">
                      <label>
                        <input type="checkbox" v-model="selectAll" @click="select">
                      </label>
                    </th>
                    <th class="QuestionID">Question ID</th>
                    <th class="Question">Question</th>
                    <th class="Answer">Answer A</th>
                    <th class="Answer">Answer B</th>
                    <th class="Answer">Answer C</th>
                    <th class="Answer">Answer</th>
                  </tr>
                </thead>
                <tbody>
                  <tr v-for="(item, index) in resultQuery" :key="index">
                    <td>{{index + 1}}</td>
                    <td>
                      <label>
                        <input v-model="selected" :value="item.QuestionID" type="checkbox" @change="show">
                      </label>
                    </td>
                    <td>{{ item.QuestionID }}</td>
                    <td>{{ item.Question }}</td>
                    <td>{{ item.A }}</td>
                    <td>{{ item.B }}</td>
                    <td>{{ item.C }}</td>
                    <td>{{ item.Answer }}</td>
                  </tr>
                </tbody>
              </table>
          </div>
        </div>
        <!-- Pagination -->
        <div class="overflow-auto">
          <b-pagination v-model="currentPage" :total-rows="rows" :per-page="perPage" aria-controls="my-table"></b-pagination>
          <p class="mt-3">Current Page: {{ currentPage }}</p>
          <b-table id="my-table" :items="items" :per-page="perPage" :current-page="currentPage" small></b-table>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios';
export default {
    name: 'questionlist',
    data() {
      return {
        keyword: '',
        selectAll: false,
        selected: [],
        alertMessage: 'Calling APIs Successful !',
        // Pagination
        perPage: 3,
        currentPage: 1,
        items: [
          { id: 2, first_name: 'Wilma', last_name: 'Flintstone' },
          { id: 3, first_name: 'Barney', last_name: 'Rubble' },
          { id: 4, first_name: 'Betty', last_name: 'Rubble' },
          { id: 5, first_name: 'Pebbles', last_name: 'Flintstone' },
          { id: 6, first_name: 'Bamm Bamm', last_name: 'Rubble' },
          { id: 7, first_name: 'The Great', last_name: 'Gazzoo' },
          { id: 8, first_name: 'Rockhead', last_name: 'Slate' },
          { id: 9, first_name: 'Pearl', last_name: 'Slaghoople' }
        ]
      }
    },
    methods: {
      select() {
        this.selected = [];
        if (!this.selectAll) {
          for (let i in this.items) {
            this.selected.push(this.items[i].QuestionID);
          }
        }
        console.log(this.selected)
      },

      show() {
        console.log(this.selected)
      }
    },
    computed: {
      resultQuery() {
        if(this.keyword) {
          return this.items.filter((item) => {
            return this.keyword.toLowerCase().split(' ').every(v => item.Question.toLowerCase().includes(v))
          })
        }else {
          return this.items
        }
      },
      rows() {
        return this.items.length
      }
    },
    mounted() {
      axios.get(`https://fb690f6085ad.ngrok.io/getAllQuestionList`)
      .then(response => { this.items = response.data }).then(()=> {window.alert(this.alertMessage)})

    },
    
}
</script>

<style>

</style>

<style scoped src="../assets/css/QuestionList.css"></style>
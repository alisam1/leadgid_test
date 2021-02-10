<template>
  <div class="content-area">
    <main class="site-main">
      <div
      v-for="item in paginatedCards"
      :key="item.id"
      class="grid portfoliogrid">
        <article class="hentry">
          <header class="entry-header">
            <div class="entry-thumbnail">
              <a href="#"><img v-bind:src="item.thumbnailUrl" alt="" /></a>
            </div>
            <h2 class="entry-title"><a href="#" rel="bookmark">{{item.title}}</a></h2>
          </header>
        </article>
      </div>
      <br />
    </main>
    <div class="pagination">
        <div class="pagination__page"
          v-for="page in pages"
          :key="page"
          @click="pageClick(page)">
            <button>{{page}}</button>
        </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'Card',
  data() {
    return {
      items: [],
      cardsPerPage: 10,
      pageNumber: 1
    }
  },
  async mounted() {
    const items = await this.$axios.$get('http://jsonplaceholder.typicode.com/photos');
    this.$set(this, 'items', items.slice(0, 50));
    return this.items;
  },
  computed: {
      pages(){
          return Math.ceil(this.items.length / 10)
      },
      paginatedCards(){
          let from = (this.pageNumber - 1) * this.cardsPerPage;
          let to = from + this.cardsPerPage;
          return this.items.slice(from,to)
      }
  },
  methods: {
      pageClick(page){
          this.pageNumber = page
      }
  },

}
</script>

<style lang="scss">

.site-main{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    flex-wrap: wrap;
    margin-top: 50px;
}

.portfoliogrid {
  width: 33%;
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
}

.hentry {
  margin: 0 0 30px;
  width:80%;
  max-width: 100%;
}

.entry-header{
    display: flex;
    flex-direction: column;
    align-items: center;
}

.entry-thumbnail {
  padding: 0 0 0em 0;
}

.entry-title {
  line-height: 1.4;
  margin-top: 0;
  margin-bottom: 0;
  text-transform: uppercase;
  font-style: normal;
  letter-spacing: 1px;
  text-align: center;
  font-size: 14px;
  color: #111;
  font-weight: 400;
}

.entry-title a {
  text-decoration: none;
  color: inherit;
}

.entry-title a:hover {
  color: #ccc !important;
}

/* Pagintaion */
.pagination{
    display: flex;
    flex-direction: row;
    justify-content: center;
    &__page{
        margin-right: 20px;
        button{
            width: 40px;
            height: 40px;
            border: none;
            background: #142bfc;
            color: #fff;
            font-size: 16px;
            cursor: pointer;
            border-radius: 5px;
            border: 1px solid transparent;
            &:hover{
                background: inherit;
                border: 1px solid #142bfc;
                color: #142bfc;
            }
            &:active{
                background: inherit;
                border: 1px solid #142bfc;
                color: #142bfc;
            }
        }
    }
}
</style>

<template>
  <v-row>
    <v-col cols="7">
      <v-row>
        <v-col cols="12" class="mb-0 mt-5">
          <div class="ml-5">
            <new-tweet></new-tweet>
          </div>
        </v-col>
      </v-row>
      <v-row>
        <v-col cols="12">
          <div>

            <div
              v-for="post in posts"
              :key="post.id"
              class="my-5"
            >
              <tweet-card></tweet-card>

            </div>

            <div v-if="loading" class="loading-spinner">
              <!-- Show a loading spinner or loading indicator here -->
            </div>
          </div>
        </v-col>
      </v-row>
    </v-col>
    <v-col cols="5">
      <div class="mt-5 mr-15">
        <search-box></search-box>
      </div>
      <div class="pt-5 pr-10">
        <trendings-card></trendings-card>
      </div>
      <div class="pt-5 pr-10">
        <to-follow></to-follow>
      </div>

    </v-col>
  </v-row>
</template>

<script>
import TweetCard from "@/components/TweetCard";
import NewTweet from "@/components/NewTweet";
import SearchBox from "@/components/SearchBox";
import TrendingsCard from "@/components/TrendingsCard";
import ToFollow from "@/components/ToFollow";
export default {
  components: {ToFollow, TrendingsCard, SearchBox, NewTweet, TweetCard},
  data() {
    return {
      posts: [
        {
          id: 1
        },
        {
          id: 2
        },
        {
          id: 2
        },
        {
          id: 2
        },
        {
          id: 2
        },
        {
          id: 2
        },
        {
          id: 2
        },
        {
          id: 2
        },
      ],
      loading: false,
      page: 1,
      totalPages: 0
    };
  },
  mounted() {
    this.fetchPosts();
  },
  methods: {
    fetchPosts() {
      // Simulating API call delay
      setTimeout(() => {
        // Replace this code with your actual API call
        // Adjust the parameters according to your API pagination
        const pageSize = 10;

        // Fetch posts for the current page
        // Assuming the API returns the total number of pages
        const apiResponse = this.getPostsFromApi(this.page, pageSize);
        this.posts = this.posts.concat(apiResponse.posts);
        this.totalPages = apiResponse.totalPages;

        this.loading = false;
      }, 1000); // Simulated delay of 1 second
    },
    getPostsFromApi(page, pageSize) {
      // Replace this with your actual API call to fetch posts
      // Return an object with posts for the current page and total pages
      // Example response format:
      return {
        posts: [
          // Array of post objects
        ],
        totalPages: 5 // Total number of pages available in the API
      };
    },
    loadMore() {
      if (!this.loading && this.page < this.totalPages) {
        this.page++;
        this.loading = true;
        this.fetchPosts();
      }
    }
  },
  directives: {
    InfiniteScroll: {
      inserted(el, binding) {
        const f = binding.value;
        el.addEventListener('scroll', function() {
          if (el.scrollTop + el.clientHeight >= el.scrollHeight) {
            f();
          }
        });
      }
    }
  },
  created() {
    window.addEventListener('scroll', this.loadMore);
  },
  beforeDestroy() {
    window.removeEventListener('scroll', this.loadMore);
  }
};
</script>


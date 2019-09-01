# Mutation 

This lab explore how we can use mutation to create content on our blog.  

```

mutation {
  createPost(input: {body: "' -- ", title: "test_title", authorId: 2}) {
    post {
      body
      authorId
      title
    }
  }
}

```


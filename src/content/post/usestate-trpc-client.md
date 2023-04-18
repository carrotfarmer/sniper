---
title: "tRPC useState client"
publishDate: "18 Apr 2023"
description: "Handle tRPC queries and mutations with useState" 
tags: ["trpc", "t3", "nextjs", "chakra-ui", "react", "typescript"]
---

```tsx
export const Posts = () => {
  const [posts, setPosts] = React.useState<
    (IPost & {
      author: User;
      likedBy: User[];
    })[]
  >([]);

  const {
    data: postsData,
    isLoading,
    isFetching,
  } = trpc.post.getPosts.useQuery();

  if (isFetching && isLoading) {
    return (
      <Center pt="10">
        <Spinner />
      </Center>
    );
  }

  if (posts.length === 0 && postsData) {
    setPosts(postsData);
  }

  return (
    <div>
      <Box>
        <Center>
          <VStack>
            {postsData &&
              posts.map((posts) => (
                <Post
                  post={post}
                  key={post.id}
                  author={post.author}
                  setPosts={setPosts}
                  likedBy={post.likedBy}
                />
              ))}
          </VStack>
        </Center>
      </Box>
    </div>
  );
};
```

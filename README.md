In one week we created a mock-up Social Media App named Motion.

Front-end Framework/Library:
* React.

Fetching:

* Axios

Styling:

* Styled Components

State Management:

* Redux
* React-redux
* edux-thunk
* Redux-devtools-extension

Routing:

* React-router

Tools:
* Polished (pixels convertion to rem)


Backend:
Django.


ENDPOINTS:

Posts

/backend/api/social/posts/ POST: user can make a new post by sending post data
/backend/api/social/posts/ GET: lists all the posts of all users in chronological order
/backend/api/social/posts/<int:post_id> GET: get a specific post by ID and display all the information about that post
/backend/api/social/posts/<int:post_id> PATCH: update a specific post (only allow owner of post or admin)
/backend/api/social/posts/<int:post_id> DELETE: delete a post by ID (only allow owner of post or admin)
/backend/api/social/posts/toggle-like/<int:post_id>/ POST: toggle like/unlike a post
/backend/api/social/posts/likes/ GET: the list of the posts the user likes
/backend/api/social/posts/following/ GET: the list of the posts from users that the current user is following
/backend/api/social/posts/user/<int:user_id> GET: the list of all posts from a given user in chronological order

Users

/backend/api/users/ GET: Get all the users
/backend/api/social/followers/toggle-follow/<int:user_id>/ POST: toggle follow/unfollow a user
/backend/api/social/followers/followers/ GET: list of all the followers
/backend/api/social/followers/following/ GET: list of all the people the user is following


Follow

/api/social/toggle-follow/<int:user_id>/ POST: Toggle following a user
/api/social/followers/followers/ GET: List of all the logged in user’s followers
/api/social/followers/following/ GET: List of all the users the user is following


Friends

/api/social/friends/request/<int:user_id>/ POST: Send friend request to another user
/api/social/friends/requests/<int:friend_request_id>/ GET,PATCH,DELETE: Get Update (Accept, Reject) or Delete an open friend request
/api/social/friends/requests/?status=<str:status> GET: List of all friend requests logged in user is in  filtered by status
/api/social/friends/ GET: List all accepted friends¨


Comments

/api/social/comments/<int:post_id>/ GET, POST: Create new post or get all comments of a post.

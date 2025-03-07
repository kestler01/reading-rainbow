# reading-rainbow

OVERVIEW
------------------
Reading Rainbow is an app inspired my own love of reading and is meant to harken back to the childhood joy of earning rewards based on how many books you read each summer. It is used to track what books you have read and what you are wanting to read next, as well as which ones you personally own.

TECHNOLOGIES USED
------------------
  -HTML5
  -CSS
  -Javascript
  -Express
  -Liquid
  -Mongoose



```const BookSchema = new Schema({
    title: String,
    author: String,
    pages: Number,
    genre: String,
    owned: Boolean,
    owner: {
        type: Schema.Types.ObjectId,
        ref: 'User'
    },
    review: [reviewSchema]

}
const reviewSchema = new Schema({
    rating: {
        type: Number,
        enum: [1, 2, 3, 4, 5]
    },
    review: {
        type: String,
    },
    readDate: {
      type: Date,
      required: true
    },
    author: {
        type: Schema.Types.ObjectId,
        ref: 'User',
        required: true
    }
}, {
    timestamps: true
})
```


USER STORIES
-----------------
As a user I want:
  - to be able to sign up
  - to be able to login and logout
  - to be able to search for books
  - to be able to add book to my shelves (Want to Read, Read)
  - be able to look at shelves one by one
  - be able to view my progress towards reading goal 
  - be able to mark a book as owned
  -  beable to filter shelves by owned books
  - be able to view book info
  - be able to leave a review/comments about read books
  - be able to edit or delete their own review/comment
  - be able to remove book from their shelves
  - view other users reviews of books
  - make a reading goal
  - track progress on reading goal

WIREFRAMES
----------------
![image](https://user-images.githubusercontent.com/112446901/194789038-327123ff-2609-41f0-b279-50f1743aebd9.png)
![image](https://user-images.githubusercontent.com/112446901/194789052-371f5f7f-92fe-45a6-b705-1589afe3e2bc.png)
![image](https://user-images.githubusercontent.com/112446901/194789070-6d35d9dc-d42d-4485-97ba-d047a1d58fdf.png)
![image](https://user-images.githubusercontent.com/112446901/194789087-4467668e-e84d-4d79-8567-a3c4f41b7296.png)
![image](https://user-images.githubusercontent.com/112446901/194789099-0c1cf93e-2c67-4d65-9cc7-00739596d7d3.png)


ERDs
----------------

![image](https://user-images.githubusercontent.com/112446901/194789546-a5aa63a6-e5c5-4552-ae69-f14204389da5.png)
![image](https://user-images.githubusercontent.com/112446901/194790163-696dc3e4-2c78-4d97-9592-85a43e554c2a.png)

SCHEDULE
------------------
  - Monday: get approval, download boilerplate, edit boilerplate and add schemas for reviews
  - Tuesday: build bones of routes, refer back to projects
  - Wednesday: polish routes, fix whatever routes aren't working
  - Thursday: work on liquid view
  - Friday: work on liquid view



<!-- @format -->

# swe-sr-8-1

For guidance on setting up and submitting this assignment, refer to the Marcy lab School Docs How-To guide for [Working with Short Response and Coding Assignments](https://marcylabschool.gitbook.io/marcy-lab-school-docs/fullstack-curriculum/how-tos/working-with-assignments#how-to-work-on-assignments).

## Prompt

![Fullstack Diagram](./client-server-database-diagram.svg)

You’ve been given a diagram (see above) showing the three core layers of a fullstack application:

- Frontend – a React application that users interact with
- Backend – an Express server that handles logic and communication
- Database – a PostgreSQL database that stores persistent data

Imagine you’re explaining how these layers work together by using a real-world example: Instagram.

Your task:

1. Explain how Instagram works using the three-layer diagram.

   - What happens when a user opens the app, scrolls through their feed, likes a post, or uploads a new photo?
   - Walk through how data flows from the frontend to the backend and to the database—and back again.

2. Come up with an analogy to help someone new to coding understand these layers.

- You might compare the system to something like a restaurant, a library, or even a post office—anything that helps make the roles of each layer intuitive.
- Make sure your analogy maps clearly to the roles of the frontend, backend, and database.

3. Reflect on the value of this separation.

- Why do we separate concerns into these layers?
- What would go wrong if we tried to do everything in one layer?

Audience: Imagine you're writing this for someone who's just starting out in web development and wants to understand how modern apps work.

Length: Around 400–600 words.

Response:

1. When you upload a new post on Instagram, there’s a three-step process that takes place. You’re interacting with the frontend—the Instagram app you see—when you tap the “+” button to create a new post. That action sends a request to Instagram’s backend, which handles what kind of operation the user is trying to perform. In this case, it’s a Create request, following the CRUD model (Create, Read, Update, Delete). The backend then prepares a query to the database to save the new post and update your account with a reference to that post.

   Once the database stores the data, it sends a response back to the backend confirming the operation. The backend then sends this response to the frontend, updating the app so you can immediately see your new post appear. This same cycle happens in other actions too, like scrolling (Read), liking a post (Update), or deleting content (Delete).

2. To understand how the three layers of an application—frontend, backend, and database—work together, think of it like a post office. The frontend is the part you see and interact with: the lobby, the counters, and the staff. You walk up to a representative and request a package from your P.O. box. This is like the frontend sending a request to the backend.

   The backend is the representative, who processes your request and heads into the back area of the post office. There, they access the P.O. boxes, which represent the database, where all the stored packages (data) live. The representative finds the right package based on your request, retrieves it from the database, and brings it back to the frontend—the lobby—where you receive your package.

   Each layer works together behind the scenes to fulfill your request quickly and smoothly, just like in an app. Separating the lobby, staff, and storage makes everything more organized and efficient—just like separating the frontend, backend, and database in an app.

3. We separate concerns into different layers to stay organized and build systems more effectively. Each part—the frontend, backend, and database—has a clear role, making it easier to understand, maintain, and grow the application. Separation also allows flexibility and scalability as the app gets bigger. It helps with team collaboration too, making it easier for developers to understand the code, work independently, and avoid confusion when navigating different parts of the system.

   If we tried to do everything in one layer, the code would quickly become messy and tangled—like spaghetti. It would be hard to read, debug, and update, since a small change could accidentally break other parts of the app. Without clear separation, the app would struggle to scale as it grows. Security would also suffer, since the frontend could directly access the database without any protection, making it easier for users to hack or steal sensitive information.

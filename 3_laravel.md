# crash course on laravel

> https://laraveldaily.com/roadmap-learning-path
> 
> https://github.com/LaravelDaily/Laravel-Roadmap-Learning-Path

# Setup
> Download and setup herd https://herd.laravel.com/
w

Laravel is a PHP framework that handles all the backend work your frontend needs—databases, authentication, APIs, business logic.

- MVC architecture
- REST API


REST stands for **Representational State Transfer**. It's a way to structure how your frontend and backend talk to each other.

Instead of your frontend making random requests like "give me the user data" or "save this comment," REST uses standard HTTP methods and URLs to communicate in a predictable way.

You organize your data into **resources** (users, posts, comments, etc.) and use HTTP methods to perform actions on them:

- **GET** = fetch/read data
- **POST** = create something new
- **PUT/PATCH** = update existing data
- **DELETE** = remove data

## Real example

Say you're building a blog. With REST, your endpoints might look like:

- `GET /api/posts` → get all posts
- `GET /api/posts/5` → get post with id 5
- `POST /api/posts` → create a new post
- `PUT /api/posts/5` → update post 5
- `DELETE /api/posts/5` → delete post 5


| Topic | Learning Links |
| ----- | ----- |
| **Routing and Controllers: Basics** | [Let's Test Your Laravel Routing Skills: Complete 12 Tasks](https://www.youtube.com/watch?v=pENlD3izA3Q) |
| Callback Functions and Route::view() |[Basic Routing](https://laravel.com/docs/routing#basic-routing) <br>[View Routes](https://laravel.com/docs/routing#view-routes) <br>|
| Routing to a Single Controller Method |[Basic Controllers with Routes](https://laravel.com/docs/controllers#basic-controllers) <br>|
| Route Parameters |[Route Parameters](https://laravel.com/docs/routing#route-parameters) <br>|
| Route Naming |[Names Routes](https://laravel.com/docs/routing#named-routes) <br>  [Laravel: Why You Need Route Names?](https://www.youtube.com/watch?v=7lalb6HtR1c) <br>|
| Route Groups |[Route Groups](https://laravel.com/docs/routing#route-groups) <br>  [Laravel Route Grouping: Simple to Very Complex](https://www.youtube.com/watch?v=I6kyfSmPhn8) <br>  [More videos](videos/route-groups.md) |
| **Blade Basics** | [Let's Test Your Laravel Blade Skills: Complete 8 Tasks](https://www.youtube.com/watch?v=P8s7UHuUhbg)<br> [9 Quick Tips about Laravel Blade](https://www.youtube.com/watch?v=-Glz1InN68o) <br>|
| Displaying Variables in Blade |[Blade: Displaying Data](https://laravel.com/docs/blade#displaying-data) <br>|
| Blade If-Else and Loop Structures |[Blade: If-Statements](https://laravel.com/docs/blade#if-statements) <br>[Blade Loops](https://laravel.com/docs/blade#loops) <br>|
| Layout: @include, @extends, @section, @yield |[Blade: Layout Using Template Inheritance](https://laravel.com/docs/blade#layouts-using-template-inheritance) <br>|
| Blade Components |[Blade Components](https://laravel.com/docs/blade#components) <br> [Laravel Blade Components: Two Examples - Laravel Breeze/UI](https://www.youtube.com/watch?v=HybWBINeXMw) <br>|

> Extensions to have before u work on laravel: https://www.youtube.com/watch?v=4DfrsWns6Ew 
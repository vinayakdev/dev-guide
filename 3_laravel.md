# crash course on laravel

> https://laraveldaily.com/roadmap-learning-path
> 
> https://github.com/LaravelDaily/Laravel-Roadmap-Learning-Path

# Setup
> Download and setup herd https://herd.laravel.com/


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
| **Auth Basics** | [Test Your Laravel Auth Skills: Complete 7 Tasks](https://www.youtube.com/watch?v=v_3NmwtN_S0)<br> [8 Tips & Tricks about Laravel Auth](https://www.youtube.com/watch?v=-dpp4CJS6Vk) <br> |
| Starter Kits: Breeze (Tailwind) or Laravel UI (Bootstrap) |[Laravel Breeze Official Documentation](https://laravel.com/docs/starter-kits#laravel-breeze) <br>[Laravel UI: Official Github Page](https://github.com/laravel/ui) <br>  [Laravel 8 Auth: 5 "Latest" Things You Need to Know](https://www.youtube.com/watch?v=L1FVdHdEm_8) <br> [More videos](videos/auth-starter-kits.md)<br>|
| Default Auth Model and Access its Fields from Anywhere |[Retrieving the Authenticated User](https://laravel.com/docs/authentication#retrieving-the-authenticated-user) <br>|
| Check Auth in Controller / Blade |[Determining If The Current User Is Authenticated](https://laravel.com/docs/authentication#determining-if-the-current-user-is-authenticated) <br>[Blade: Authentication Directives](https://laravel.com/docs/blade#authentication-directives) <br>|
| **Database Basics** ||
| Database Migrations |[Test Your Laravel Migrations Skills: Complete 10 Tasks](https://www.youtube.com/watch?v=tPU1hNKI_lc)<br>[Database Migrations](https://laravel.com/docs/migrations) <br>  [Laravel Migrations: Table Created but Foreign Key Failed?](https://www.youtube.com/watch?v=DWzUBpsEEHY) <br> [More videos](videos/database-migrations.md) |
| Basic Eloquent Model and MVC: Controller -> Model -> View |[Test Your Eloquent Basic Skills: 11 Tasks to Complete](https://www.youtube.com/watch?v=AmvLs9sRSH8)<br>[Eloquent: Getting Started](https://laravel.com/docs/eloquent) <br>|
| Eloquent Relationships: belongsTo / hasMany / belongsToMany |[Test Your Eloquent Relationships Skills: 9 Tasks to Complete](https://www.youtube.com/watch?v=ohj0Mc09DyE)<br>[Eloquent Relationships: One-to-One](https://laravel.com/docs/eloquent-relationships#one-to-one) <br>[Eloquent Relationships: One-to-Many](https://laravel.com/docs/eloquent-relationships#one-to-many) <br>[Eloquent Relationships: BelongsTo](https://laravel.com/docs/eloquent-relationships#one-to-many-inverse) <br>[Eloquent Relationships: Many-to-Many](https://laravel.com/docs/eloquent-relationships#many-to-many) <br>  [How to Safely Change DB Relations in Live Laravel Project?](https://www.youtube.com/watch?v=nRmoywPJRdM) |
| Eager Loading and N+1 Query Problem |[Relationships: Eager Loading](https://laravel.com/docs/eloquent-relationships#eager-loading) <br>  [Laravel N+1 Query Detector: Don't Forget Eager Loading](https://www.youtube.com/watch?v=MbN7BIcUnPA) <br>|
| **Full Simple CRUD** ||
| Route Resource and Resourceful Controllers |[Laravel Resource Controllers](https://laravel.com/docs/controllers#resource-controllers) <br>:page_facing_up: [Simple Laravel CRUD with Resource Controllers [digitalocean.com]](https://www.digitalocean.com/community/tutorials/simple-laravel-crud-with-resource-controllers) <br>  [Laravel Nested Resource Controllers: Two-Level Deep](https://www.youtube.com/watch?v=9R_9Xe3Fgnw) <br>  [More videos](videos/route-resource-resourceful-controllers.md) <br>|
| Forms, Validation and Form Requests |[Test Your Laravel Validation Skills: Complete 9 Tasks](https://www.youtube.com/watch?v=3ihjumeOMV4)<br>[Laravel Validation](https://laravel.com/docs/validation) <br>  [New in Laravel 6.13: Format Validation Error Field Name](https://www.youtube.com/watch?v=KD1SqLO58eE)  [More videos](videos/forms-validation-requests.md) |
| File Uploads and Storage Folder Basics |[Test Your Laravel File Upload Skills: Complete 7 Tasks](https://www.youtube.com/watch?v=_SrQRnOx3q8)<br>[Filesystem: File Uploads](https://laravel.com/docs/filesystem#file-uploads) <br>  [Laravel: How to Upload File During User Registration](https://www.youtube.com/watch?v=xyQT2pnv_4E) <br> [More videos](videos/file-uploads-and-storage-folder-basics.md) <br> |
| Table Pagination |[Database Pagination](https://laravel.com/docs/pagination) <br>|

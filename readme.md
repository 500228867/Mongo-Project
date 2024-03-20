Project: Golden Rule: 
Emphasize the importance of storing data together that is frequently accessed together, reinforcing the golden rule of MongoDB data modeling
# MongoDB Document Database Design Project

## Title
Golden Rule: Emphasize the importance of storing data together that is frequently accessed together, reinforcing the golden rule of MongoDB data modeling.

## Executive Summary
This project aims to demonstrate the importance of storing data together that is frequently accessed together, following the Golden Rule of MongoDB data modeling. By organizing related data into collections and documents, we can improve query performance and optimize data retrieval operations.

## Project Requirements
1. Design a MongoDB document database.
2. Create five collections to store related data.
3. Implement the Golden Rule of data modeling to emphasize storing frequently accessed data together.

## Data Model
### Collection 1: Users
- **Fields:**
  - `_id`: ObjectId (Primary key)
  - `username`: String
  - `email`: String
  - `password`: String
  - `created_at`: Date
- **Explanation:** Stores user information such as username, email, password, and creation date.

### Collection 2: Posts
- **Fields:**
  - `_id`: ObjectId (Primary key)
  - `title`: String
  - `content`: String
  - `author_id`: ObjectId (Reference to Users collection)
  - `created_at`: Date
- **Explanation:** Contains posts created by users, linked to the Users collection by author_id.

### Collection 3: Comments
- **Fields:**
  - `_id`: ObjectId (Primary key)
  - `content`: String
  - `post_id`: ObjectId (Reference to Posts collection)
  - `user_id`: ObjectId (Reference to Users collection)
  - `created_at`: Date
- **Explanation:** Stores comments made by users on posts, linked to both Posts and Users collections.

### Collection 4: Products
- **Fields:**
  - `_id`: ObjectId (Primary key)
  - `name`: String
  - `description`: String
  - `price`: Number
  - `category`: String
- **Explanation:** Contains information about products available in an e-commerce platform.

### Collection 5: Orders
- **Fields:**
  - `_id`: ObjectId (Primary key)
  - `user_id`: ObjectId (Reference to Users collection)
  - `products`: Array of Objects
    - `product_id`: ObjectId (Reference to Products collection)
    - `quantity`: Number
- **Explanation:** Tracks orders placed by users, including the products ordered and their quantities.

## Conclusion
By following the Golden Rule of data modeling in MongoDB, we can create a well-organized document database structure that optimizes data retrieval and enhances overall system performance. Storing related data together in collections helps in efficient querying and improves the scalability and maintainability of the database.

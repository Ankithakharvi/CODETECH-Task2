

---

**Project Name:** Online Book Mart

**Name:** Ankitha

**ID:** CT08DS2403

**Company:** CODTECH IT SOLUTIONS

**Domain:** Web Development

**Duration:**  June 15th - July 15th 2024

**Mentor:** Neela Santhosh Kumar

---

**Objective:**

Develop an online book mart web application with comprehensive features for users and administrators, including user registration, book browsing, ordering, messaging, and payment integration.

---
user dashbord
<img width="960" alt="Screenshot 2024-07-15 200837" src="https://github.com/user-attachments/assets/8a5d4505-358b-4b9a-b847-9cd9e592b5cd">
<img width="960" alt="Screenshot 2024-07-15 200905" src="https://github.com/user-attachments/assets/a42aedac-d855-4225-9d51-8a7c6e8a2d4e">

 <img width="960" alt="Screenshot 2024-07-15 200916" src="https://github.com/user-attachments/assets/ef8db899-a8f3-4568-9a59-1af9adaadf40">

 
 <img width="960" alt="Screenshot 2024-07-15 200943" src="https://github.com/user-attachments/assets/7a24d3ce-27ba-40b1-b932-091320de832e">

 <img width="960" alt="Screenshot 2024-07-15 200957" src="https://github.com/user-attachments/assets/f4e1b80a-d0d9-4f94-be06-5f7cc4299ede">
 <img width="960" alt="Screenshot 2024-07-15 200905" src="https://github.com/user-attachments/assets/5de175c2-9b72-40b1-9d13-957bdc73e5da"> 
  admin dashboard
  
<img width="960" alt="Screenshot 2024-07-15 201105" src="https://github.com/user-attachments/assets/8297f0c5-6e57-4f0e-87a9-edcbf4847774">

<img width="960" alt="Screenshot 2024-07-15 201125" src="https://github.com/user-attachments/assets/8a40636d-0df9-4ea1-b5ee-181305f3a531">


<img width="960" alt="Screenshot 2024-07-15 201140" src="https://github.com/user-attachments/assets/799f2e27-5c48-4233-8abf-4487bbae863e">


<img width="960" alt="Screenshot 2024-07-15 201151" src="https://github.com/user-attachments/assets/e911ae99-b14a-49b0-93cd-42a05dbd5d7e">
<img width="960" alt="Screenshot 2024-07-15 201202" src="https://github.com/user-attachments/assets/971c4117-85c9-427b-9b4b-3b5b9f6bc94e">

**Functionality:**

- **User Authentication:**
  - Users can register and log in with email/password credentials.
  - Passwords are securely stored and hashed.
  - Users can reset passwords via email.
  
- **User Features:**
  - **Book Browsing:** Browse books by category, author, or title.
  - **Book Details:** View detailed information about each book, including price, author, and availability.
  - **Cart Management:** Add books to the cart, update quantities, and remove items.
  - **Order Placement:** Checkout with selected items, providing shipping details.
  - **Order Summary:** After checkout, display the total amount price including all selected items.
  - **Messaging:** Send messages to the admin regarding orders or inquiries.
  - **Payment Integration:** Secure payment gateway integration for processing orders.
  
- **Admin Features:**
  - **Admin Login:** Secure login for administrators with separate privileges.
  - **Book Management:** Add new books with details (title, author, price, etc.), edit existing book information, and delete books.
  - **Order Management:** View and manage incoming orders, update order status (processing, shipped, delivered).
  - **User Management:** View registered users, edit user details, and disable accounts if necessary.
  - **Messaging:** Receive and respond to messages from users.
  
---

**Database Structure Documentation:**

**Database Name:** `shop_db`

**Tables:**

1. **Table: `cart`**
   - Description: Stores items added to the cart by users.
   - Columns:
     - `id`: Primary key, unique identifier for each cart item.
     - `user_id`: Foreign key referencing `users.id`, identifies the user who added the item.
     - `name`: Name of the product.
     - `price`: Price of the product.
     - `quantity`: Quantity of the product.
     - `image`: Path to the image of the product.

2. **Table: `message`**
   - Description: Stores messages sent by users to administrators.
   - Columns:
     - `id`: Primary key, unique identifier for each message.
     - `user_id`: Foreign key referencing `users.id`, identifies the user who sent the message.
     - `name`: Name of the user who sent the message.
     - `email`: Email of the user who sent the message.
     - `number`: Contact number of the user who sent the message.
     - `message`: Content of the message.

3. **Table: `orders`**
   - Description: Stores details of orders placed by users.
   - Columns:
     - `id`: Primary key, unique identifier for each order.
     - `user_id`: Foreign key referencing `users.id`, identifies the user who placed the order.
     - `name`: Name of the user who placed the order.
     - `number`: Contact number of the user who placed the order.
     - `email`: Email of the user who placed the order.
     - `method`: Payment method chosen by the user.
     - `address`: Shipping address provided by the user.
     - `total_products`: JSON array storing details (id, name, quantity) of products ordered.
     - `total_price`: Total price of the order.
     - `placed_on`: Date and time when the order was placed.
     - `payment_status`: Status of the payment (default: pending).

4. **Table: `products`**
   - Description: Stores details of available products.
   - Columns:
     - `id`: Primary key, unique identifier for each product.
     - `name`: Name of the product.
     - `price`: Price of the product.
     - `image`: Path to the image of the product.

5. **Table: `users`**
   - Description: Stores details of registered users.
   - Columns:
     - `id`: Primary key, unique identifier for each user.
     - `name`: Name of the user.
     - `email`: Email address of the user.
     - `password`: Encrypted password of the user.
     - `user_type`: Type of user (default: user, can be admin).

**Indexes:**

Each table has a primary key index on the `id` column for unique identification.

**Auto Increment:**

- `id` columns in all tables are set to auto increment for automatic generation of unique identifiers.

**SQL Dump Version:**
- **Version**: 5.1.1
- **Server**: MariaDB 10.4.22
- **PHP Version**: 8.1.2

 

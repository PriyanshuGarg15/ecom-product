# Product Microservice

The Product microservice is responsible for managing product-related operations, providing functionalities to retrieve product information, create new products, update existing ones, and handle product reviews.

## Access

The microservice is hosted on AWS ECS Docker at the following URL:

http://ecom-user-lb-321143357.ap-south-1.elb.amazonaws.com:4041

## Routes

### Get Products

- **Route**: `/api/products`
- **Method**: GET
- **Description**: Retrieve a list of available products.

### Get All Products

- **Route**: `/api/products/all`
- **Method**: GET
- **Description**: Retrieve details of all products, including those that may be hidden or inactive.

### Admin Routes

#### Create Product

- **Route**: `/api/admin/product/new`
- **Method**: POST
- **Description**: Add a new product to the system. (Requires admin privileges)

#### Update, Delete Product

- **Route**: `/api/admin/product/:id`
- **Method**: 
  - PUT: Update details of a specific product.
  - DELETE: Remove a product from the system. (Requires admin privileges)

#### Get Admin Products

- **Route**: `/api/admin/products`
- **Method**: GET
- **Description**: Retrieve a list of products specifically for administrative purposes. (Requires admin privileges)

### Product Details

#### Get Product Details

- **Route**: `/api/product/:id`
- **Method**: GET
- **Description**: Retrieve detailed information about a specific product.

### Reviews

#### Create Product Review

- **Route**: `/api/review`
- **Method**: PUT
- **Description**: Submit a review for a product. (Authentication required)

#### Admin Reviews

- **Route**: `/api/admin/reviews`
- **Method**: 
  - GET: Retrieve all product reviews.
  - DELETE: Delete a product review. (Requires admin privileges)

## Dependencies

- Express.js: Web framework for Node.js
- Mongoose: MongoDB object modeling tool
- cloudinary: ^2.0.3
- express: ^4.19.2
- express-rate-limit: ^7.2.0

## Usage

1. Clone the repository.
2. Install dependencies using `npm install`.
3. Set environment variables.
4. Run the microservice using `npm start`.

## Contributors

- [Priyanshu Garg](#) - Developer

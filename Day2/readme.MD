🌍 Marketplace Creator Hackathon - Day 2

Project Summary

This project serves as the foundation for a dynamic and scalable online marketplace, crafted as part of the Marketplace Creator Hackathon 2025. By utilizing modern technologies, the platform aims to provide users with a seamless and engaging shopping experience.

🚀 Key Features

System Framework

Robust Design: A well-structured framework that integrates frontend, backend, and external services.

Smooth Workflows: Efficient processes ensuring intuitive user interactions and system functionality.

API Endpoints

Well-documented API routes, including request parameters and example responses.

Sanity CMS Integration

Customized schemas for managing critical data such as products, customers, and orders.

System Architecture Overview

Core Components:

Frontend (Next.js): A responsive and dynamic user interface.

Sanity CMS: A flexible backend for data organization and content management.

Third-Party Integrations: Payment handling via Stripe and logistics support for order tracking.

🔄 Workflow Summary:

Users browse products, add items to their cart, and proceed to checkout.

The frontend communicates with Sanity CMS for data retrieval and updates.

Payment and shipping details are processed securely using third-party APIs.

API Endpoints

Endpoint

Method

Function

Request Body

Response Example

/products

GET

Fetch available items

N/A

{ "id": 1, "name": "Sofa", "price": 1000 }

/cart

POST

Add item to cart

{ "productId": 1, "quantity": 2 }

{ "cartId": 123, "status": "Added" }

/checkout

POST

Process transaction

{ "cartId": 123, "paymentInfo": {...} }

{ "orderId": 456, "status": "Confirmed" }

Sanity CMS Data Structures

Product Schema:

export default {
  name: 'product',
  type: 'document',
  fields: [
    { name: 'name', type: 'string', title: 'Product Name' },
    { name: 'price', type: 'number', title: 'Price' },
    { name: 'stock', type: 'number', title: 'Available Stock' },
    { name: 'image', type: 'image', title: 'Product Image' }
  ]
};

Order Schema:

export default {
  name: 'order',
  type: 'document',
  fields: [
    { name: 'customer', type: 'reference', to: [{ type: 'customer' }] },
    { name: 'products', type: 'array', of: [{ type: 'product' }] },
    { name: 'status', type: 'string', title: 'Order Status' }
  ]
};

🛒 User Flow

Steps for Users

Account Access:

Users can register or log in securely.

Login details are managed within Sanity CMS.

Cart Management:

Users can add products and modify quantities.

API routes handle cart operations effectively.

Order Processing:

Orders are confirmed at checkout and stored in the CMS.

Secure payments are processed via Stripe.

💾 Code Repository

Find the full source code, architecture diagrams, and API documentation here: GitHub Repository.

📌 Future Enhancements

Implement and validate outlined workflows.

Enhance features, such as live order tracking and inventory control.

Improve platform performance and scalability.

🛠️ Suggestions

Your feedback is valuable! Feel free to submit issues or suggest improvements for the project.

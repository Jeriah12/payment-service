# payment-Service

The **payment-service** manages the shopping cart, order placement, and order tracking functionalities within the e-commerce platform.

## Table of Contents

- [Features](#features)
- [Technology Stack](#technology-stack)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [API Endpoints](#api-endpoints)
- [Testing](#testing)


## Features

- **Payment Processing:** Simulates payment processing for orders.
- **Transaction Management** Manages order payments and updates their status.

## Technology Stack

- **Language:** Go
- **Framework:** Gin or Fiber
- **Database:** None or Redis (for session management)
- **Containerization:** Docker

## Prerequisites

Before you begin, ensure you have met the following requirements:

* Go 1.16 or higher
* Docker
* Git for version control

## Installation

Follow these steps to set up the Order Service on your local machine:

1. ***Clone the repository:***

```bash
git clone https://github.com/your-username/payment-service.git
cd payment-service
```
2. ***Install dependencies:***

```bash
go mod download
```

3. ***Environment Variables:***

Create a .env file in the root directory and add the following environment variables:

```properties
PORT=7000
PAYMENT_GATEWAY_API_KEY=your_api_key
```

4. ***Running Docker:***

Build the Docker image:

```bash
docker build -t payment-service:latest .
```

5. ***Run the Docker container:***

```bash
docker run -p 7000:7000 --env-file .env payment-service:latest
```
The service should now be accessible at http://localhost:7000

## API Endpoints

**Process a payment**
* Endpoint: POST /api/v1/payments
* Description: Processes a payment for an order.

  
## Testing
Run unit tests using:

```bash
go test ./...
```
This command will execute all tests located in the tests directory.

## About Project

REST API created with Laravel and Sanctum auth.

## Prerequired

-   **PHP**
-   **Composer**

## For testing

-   **SQLiteStudio**
-   **Postman**

## Start server

Run command `php artisan serve` in project root directory.

## Routes

All routes need header to work.

Accept application/json

### Public

Route Method Input Action
/register POST name, email, password create api_key for new user
/login POST email, password create api_key with existing user

/products GET - show all products
/products/id GET - show product
/products/search/word GET - search from product names

### Protected (requires API key)

Route Method Input Action
/products POST name, slug, price create product
/products/id PUT name, slug, price update product
/products/id DELETE - destroy product
/logout POST - destroy all API keys

# Pizzas Restaurants

This Rails API backend project, created by Bonface Mabeche, allows you to manage restaurants and their associated pizzas. It provides a set of endpoints for retrieving restaurant and pizza data, as well as creating restaurant-pizza associations.

## Requirements

To run this project, you'll need the following:

- Ruby (version 2.7.0 or higher)
- Rails (version 6.1.0 or higher)
- PostgreSQL (or any other supported database)

## Getting Started

Follow these steps to get the project up and running:

1. Clone this repository to your local machine:

   ```
   git clone https://github.com/bonfacenyatangi/PizzasRestaurantsProject.git
   ```

2. Navigate to the project directory:

   ```
   cd PizzasRestaurantsProject
   ```

3. Install the required gems by running the following command:

   ```
   bundle install
   ```

4. Set up the database by running the following commands:

   ```
   rails db:create
   rails db:migrate
   rails db:seed
   ```

   This will create the necessary database, run the migrations, and populate the database with seed data.

5. Start the Rails server:

   ```
   rails server
   ```

   The API will be accessible at `http://localhost:3000`.

## Endpoints

The following endpoints are available in this project:

- **GET /restaurants**: Retrieves a JSON array of all restaurants.

- **GET /restaurants/:id**: Retrieves a JSON object of a specific restaurant by ID, including its associated pizzas.

- **DELETE /restaurants/:id**: Deletes a specific restaurant by ID, along with its associated restaurant-pizzas.

- **GET /pizzas**: Retrieves a JSON array of all pizzas.

- **POST /restaurant_pizzas**: Creates a new restaurant-pizza association.

Please refer to the project guidelines for more details on each endpoint and their expected responses.

## Model Relationships

This project has the following model relationships:

- A `Restaurant` has many `Pizzas` through `RestaurantPizza`.
- A `Pizza` has many `Restaurants` through `RestaurantPizza`.
- A `RestaurantPizza` belongs to a `Restaurant` and belongs to a `Pizza`.

## Validations

The `RestaurantPizza` model has a validation for the `price` field, which must be between 1 and 30.

## Contributing

If you'd like to contribute to this project, you can follow these steps:

1. Fork this repository and clone it to your local machine.

2. Create a new branch for your feature or bug fix:

   ```
   git checkout -b my-feature
   ```

3. Make your changes and commit them:

   ```
   git commit -m "Add my feature"
   ```

4. Push your branch to your forked repository:

   ```
   git push origin my-feature
   ```

5. Open a pull request on GitHub and describe your changes.

## License

This project is licensed under the [MIT License](LICENSE).

Feel free to customize this README to include any additional information about your project.

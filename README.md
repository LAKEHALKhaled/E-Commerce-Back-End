# E-Commerce Back End

 Build the back end for an e-commerce site by configuring a working Express.js API to use Sequelize to interact with a MySQL database.


## Packages used

I used the [MySQL2](https://www.npmjs.com/package/mysql2) and [Sequelize](https://www.npmjs.com/package/sequelize) packages to connect the Express.js API to a MySQL database and the [dotenv](https://www.npmjs.com/package/dotenv) package to use environment variables to store sensitive data.

### Database Models

The database contain four models,  `Category`,`Product`,`Tag` & `ProductTag`

The association methods on Sequelize models create the following relationships between them:

* `Product` belongs to `Category`, and `Category` has many `Product` models, as a category can have multiple products but a product can only belong to one category.

* `Product` belongs to many `Tag` models, and `Tag` belongs to many `Product` models. Allow products to have multiple tags and tags to have many products by using the `ProductTag` through model.

### API Routes to Perform RESTful CRUD Operations

 `product-routes.js`, `tag-routes.js`, and `category-routes.js` are to perform create, read, update, and delete operations using your Sequelize models.
 after creating the models and routes, run `npm run seed` will seed data to the database.


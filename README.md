# SQL Query Handler for JavaScript

This JavaScript project provides a convenient and simple way to handle SQL queries in your applications. It consists of a concrete class that can be easily extended for each table in your database.

## Getting Started

To integrate this project into your repository, follow these steps:

1. Add this project as a git template:

   ```bash
   git remote add template https://github.com/your-template-repo.git
   git fetch template
   git merge --allow-unrelated-histories template/main
   ```


## Usage

To use this SQL query handler, follow these steps:

1. Create a class for each table you need to interact with.

2. Make these classes inherit from the provided `model` class.

3. Utilize the following methods on instances of your new inherited class objects:

   - `update`: Update a record in the database.
   - `load`: Load a single record from the database.
   - `loadmany`: Load multiple records from the database.
   - `save`: Save a new record to the database.
   - `delete`: Delete a record from the database.
4. When calling these methods use await

### Example:

```javascript
import Model from './Model.js';

export default class Task extends Model {

  static table = "schema.tasks";
  static primary = ["id"];

  // Additional methods or properties specific to the 'schema.tasks' table can be added here.
}
```

## Contributions

Feel free to contribute by submitting issues or pull requests. Any feedback or improvements are highly appreciated!

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

---

**Note:** This code is almost entirely copied from [Khoi Nguyen](https://github.com/khoi-nguyen/LW3L-orm/blob/main/models/Model.js), and I'm giving him all the credits for the original implementation.

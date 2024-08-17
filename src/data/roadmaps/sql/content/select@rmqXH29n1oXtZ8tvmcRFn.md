# Select Statement

Select Statement are used to retreive data from the database in desired manner. Select Statement in a query can retrieve a set of data with certain condition or a single record from the database. Following are a
few examples:

1. **Select All**: Select all rows from the database using **'*'**:
   
   Example:
    ```sql
    SELECT *
    FROM products;
    ```
2. **Select Specific Columns**: Select specific required columns from the database using **column_names** (Helps in optimizing a query):
   
   Example:
    ```sql
    SELECT product, price, (price * 0.18) as tax
    FROM products;
    ```

3. **Select Data with Certain Constraints**: Select Data using `where` clause:
   
   Example:
    ```sql
    SELECT product, price, (price * 0.18) as tax, is_active
    FROM products where is_active = 1;
    ```
    
4. **Select Single / Limited Record**: Select limited number of rows using `Limit` clause:

    - `AND`: Returns true if both components are true.
    - `OR` : Returns true if any one of the component is true.
    - `NOT`: Returns the opposite boolean value of the condition.

   Example:
    ```sql
    SELECT product, price, (price * 0.18) as tax, is_active
    FROM products where is_active = 1 LIMIT 1;
    ```

   ```sql
    SELECT product, price, (price * 0.18) as tax, is_active
    FROM products where is_active = 1 LIMIT 20;
    ```

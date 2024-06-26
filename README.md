# Application Overview

## Admin Section

When logging in as **admin**, you will be directed to the admin folder and to `admin.php`. Here are the main functionalities:

- **admin.php**: View counts of created categories and total products sold.
- **add-product.php**: Add new products to the system.
- **report.php**: View and manage staff reports on products. Receive email notifications for new reports.
- **daily-income.php**: View monthly profit data.
- **group-supply.php**: Manage products, including updates and deletions.
- **add-category.php**: Add new categories for products.
- **logout**: Redirects to `index.php`.

## Staff Section

When logging in as **staff**, you will be directed to the public folder and to `staff.php`. Here are the main functionalities:

- **staff.php**: View products assigned by admin and manage their quantities. Receive email notifications when a product's quantity reaches 25.
- **report.php**: Send reports to admin regarding products. Admin receives email notifications.
- **all-sales.php**: View sales data by month.
- **logout**: Redirects to `index.php`.

## Integrated Flowchart

```markdown
           +-----------------------+
           |                       |
           |       Login Page      |
           |                       |
           +-----------+-----------+
                       |
       +---------------+---------------+
       |                               |
       |         Admin Login            |
       |                               |
+------+-------+           +-----------+-----------+
|              |           |                       |
|  admin.php   |<----------+     add-product.php    |
|              |           |                       |
+------+-------+           +-----------+-----------+
       |                               |
       |                               |
+------+-------+           +-----------+-----------+
|              |           |                       |
|   report.php |           |     add-category.php   |
|              |           |                       |
+------+-------+           +-----------+-----------+
       |                               |
       |                               |
+------+-------+           +-----------+-----------+
|              |           |                       |
|  daily-income.php         |   group-supply.php     |
|              |           |                       |
+------+-------+           +-----------+-----------+
       |                               |
       |                               |
+------+-------+           +-----------+-----------+
|              |           |                       |
|  index.php   |<----------+         logout        |
|              |           |                       |
+--------------+           +-----------------------+
           ^
           |
           |
           |    +-----------------------------------+
           |    |                                   |
           +----+        Staff Login                 |
                |                                   |
                +-----------+-----------+-----------+
                            |           |
          +-----------------+           +-----------------+
          |                                                 |
          |           staff.php                             |
          |                                                 |
          +-----------------+-----------+-----------+-------+
                            |                       |
          +-----------------+                       +-----------------+
          |                                                         |
          |           report.php                                      |
          |                                                         |
          +-----------------+-----------+-----------+---------------+
                            |                       |
          +-----------------+           +-----------+-----------+
          |                             |                       |
          |         all-sales.php        |         logout        |
          |                             |                       |
          +-----------------------------+-----------------------+



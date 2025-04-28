# SmartSync-Inventory-Billing-System

[![Project Status](https://img.shields.io/badge/Status-Completed-brightgreen.svg?style=for-the-badge)](https://github.com/your-username/your-repo-name)
[![Last Commit](https://img.shields.io/github/last-commit/your-username/your-repo-name?style=for-the-badge)](https://github.com/your-username/your-repo-name/commits/main)
[![Open Issues](https://img.shields.io/github/issues/your-username/your-repo-name?style=for-the-badge)](https://github.com/your-username/your-repo-name/issues)
[![License](https://img.shields.io/github/license/your-username/your-repo-name?style=for-the-badge)](./LICENSE)

## Project Overview

The Smart Inventory and Billing System is a desktop application developed using Java and Swing for the graphical user interface. It aims to provide an efficient solution for managing inventory and generating bills for businesses. The system utilizes a MySQL database to store and retrieve data, and it includes modules for login, dashboard, product management, and billing. A detailed project report, including system analysis, diagrams, implementation details, and testing, is available in the `Documentation` folder.

## Features

* **Login Module:** Secure user authentication to access the system.
* **Dashboard:** Provides an overview of the system with key information.
* **Product Management:**
    * Add, edit, and delete product details (name, description, price, quantity).
    * View and manage current stock levels.
* **Billing Module:**
    * Create new bills by selecting products and quantities.
    * Automatic calculation of total amount.
    * Generation of bills in PDF format using iText or JasperReports.
* **MySQL Database Integration:** Persistent storage of application data (users, products, bills).
* **Swing-based GUI:** User-friendly graphical interface for easy interaction.

**Optional Add-ons (Implemented if applicable):**

* Barcode scanner integration (if implemented).
* Daily/Monthly sales reports (if implemented).
* Password reset using security questions (if implemented).
* Dark mode UI tweak (if implemented).

## Setup and Run Instructions

This section guides you on how to set up and run the Smart Inventory and Billing System on your local machine.

### Prerequisites

Ensure you have the following software installed:

* **Java Development Kit (JDK):** (Specify the version used, e.g., JDK 11 or later) - You can download it from [Oracle's website](https://www.oracle.com/java/technologies/javase-downloads.html) or [OpenAdoptium](https://adoptium.net/).
* **MySQL Server:** (Specify the version used) - Download and install from [MySQL Community Downloads](https://dev.mysql.com/downloads/community/).
* **MySQL Workbench (Optional):** A GUI tool for managing MySQL databases, helpful for setting up the database.

### Installation

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/your-username/your-repo-name.git](https://github.com/your-username/your-repo-name.git)
    cd SmartInventoryBillingSystem
    ```
    (Replace the link with your actual repository URL).

2.  **Database Setup:**
    * Ensure your MySQL server is running.
    * You can use MySQL Workbench or the command line to create the database and tables.
    * **Using the provided SQL script:**
        * Navigate to the `Database` directory:
            ```bash
            cd Database
            ```
        * Execute the `schema.sql` script to create the necessary tables. You might need to adjust the script based on your MySQL setup. For example, using the MySQL command line client:
            ```bash
            mysql -u <your_mysql_username> -p <database_name> < schema.sql
            ```
            (Replace `<your_mysql_username>` and `<database_name>` accordingly. You might need to create the database first using `CREATE DATABASE <database_name>;`).
        * (Optional) You can execute `sample_data.sql` to insert some initial data.

3.  **Import Libraries:**
    * The necessary JAR files (e.g., `mysql-connector-java-*.jar`, `itextpdf-*.jar` or `jasperreports-*.jar`) are located in the `SourceCode/lib` directory.
    * If you are using an Integrated Development Environment (IDE) like IntelliJ IDEA or Eclipse, you need to add these JAR files to your project's dependencies or classpath.

4.  **Configure Database Connection:**
    * Locate the Java source files that handle the database connection (likely in the `com.example.inventory.database` package).
    * Update the database connection details (URL, username, password) within the Java code to match your MySQL server configuration.

### Running the Application

1.  **Using an IDE (Recommended):**
    * Open the project in your preferred Java IDE (IntelliJ IDEA, Eclipse, NetBeans).
    * Ensure that the JAR files in the `SourceCode/lib` directory are added to the project's build path or dependencies.
    * Locate the main entry point of the application (usually a class with a `main` method, like `Main.java` in the `src/com/example/inventory` package).
    * Run the `Main.java` file to start the application.

2.  **Running from the Command Line:**
    * Navigate to the root directory of the project.
    * Compile the Java source files:
        ```bash
        javac -cp "SourceCode/lib/*:SourceCode/src" SourceCode/src/com/example/inventory/*.java SourceCode/src/com/example/inventory/models/*.java SourceCode/src/com/example/inventory/views/*.java SourceCode/src/com/example/inventory/controllers/*.java SourceCode/src/com/example/inventory/database/*.java SourceCode/src/com/example/inventory/utils/*.java
        ```
        (Adjust the command based on your package structure).
    * Run the application:
        ```bash
        java -cp "SourceCode/lib/*:SourceCode/src" com.example.inventory.Main
        ```
        (Replace `com.example.inventory.Main` with the actual path to your main class).

## Usage Examples/Demo

1.  **Login:** Upon starting the application, you will be presented with a login screen. Enter valid credentials to access the system.
2.  **Dashboard:** After successful login, the dashboard will display a summary of key information (if implemented).
3.  **Product Management:** Navigate to the "Products" section to add new products, view existing stock, edit product details, or delete products.
4.  **Billing:** Go to the "Billing" section to create new bills. Select products, enter quantities, and the system will calculate the total. You can then generate and save the bill as a PDF.

**Refer to the `Documentation/CompleteProjectReport.pdf` for detailed usage instructions and screenshots of the application's interface.**

## Dependencies and Configurations

* **Java:** (Specify the Java version used).
* **MySQL:** (Specify the MySQL version used). Database connection details are configured within the Java source code.
* **Swing:** The graphical user interface is built using the Java Swing library (part of the standard Java library).
* **MySQL Connector/J:** (Specify the version if known) - Used for connecting to the MySQL database. The JAR file is located in `SourceCode/lib`.
* **iText/JasperReports:** (Specify which one and the version if known) - Used for generating PDF bills. The JAR file is located in `SourceCode/lib`.

## Complete Project Report

A comprehensive project report containing:

* Cover Page, Abstract, Objective
* System Analysis
* Data Flow Diagrams (DFD - Context + Level 1)
* ER Diagram
* UML Diagrams (Use Case, Class, Activity, Sequence)
* Technologies used
* Implementation details with screenshots
* Testing procedures and results
* Future Scope
* Conclusion
* Bibliography & Appendix

is available in the `Documentation/CompleteProjectReport.pdf` file. The UML and ER diagrams can be found in the `Documentation/UMLDiagrams` directory.

## Repository Accessibility

This GitHub repository will remain **accessible at all times** for evaluation purposes.

## Contact

Rahul Kumar
rahulkr221703@gmail.com
https://github.com/rahulkr1722

Thank you for evaluating my project!

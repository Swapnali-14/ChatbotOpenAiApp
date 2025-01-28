############################# SQL###################
DB:-chatbot_db

CREATE TABLE Suppliers (
    id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(255),
    contact_info TEXT,
    product_categories_offered TEXT
);

CREATE TABLE Products (
    id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(255),
    brand VARCHAR(255),
    price DECIMAL(10, 2),
    category VARCHAR(255),
    description TEXT,
    supplier_id INT,
    FOREIGN KEY (supplier_id) REFERENCES Suppliers(id)
);




############################### Insert Queries #####################################3

INSERT INTO Suppliers (name, contact_info, product_categories_offered)
VALUES ('Supplier A', 's@gmail.com', 'Electronics, Home Appliances');

INSERT INTO Products (name, brand, price, category, description, supplier_id)
VALUES ('Smartphone', 'BrandX', 299.99, 'Electronics', 'Latest model smartphone', 1),
       ('Blender', 'BrandY', 49.99, 'Home Appliances', 'Powerful kitchen blender', 1);


##############################In app.py#########################################
Uncomment below line and add API key
# openai.api_key = "Your-api-key"






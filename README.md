# Car Rental System

A simple console-based Car Rental System implemented in Java. This system allows users to rent and return cars, providing information on rentals and calculating total prices.

## Classes

### 1. Car
- **Properties:**
  - `carId`: Unique identifier for the car.
  - `brand`: Brand of the car.
  - `model`: Model of the car.
  - `basePricePerDay`: Base rental price per day.
  - `isAvailable`: Availability status of the car.

- **Methods:**
  - `calculatePrice(int rentalDays)`: Calculate the total price for a specified number of rental days.
  - `rent()`: Mark the car as rented.
  - `returnCar()`: Mark the car as returned.

### 2. Customer
- **Properties:**
  - `customerId`: Unique identifier for the customer.
  - `name`: Name of the customer.

### 3. Rental
- **Properties:**
  - `car`: Car object being rented.
  - `customer`: Customer object renting the car.
  - `days`: Number of days for the rental.

### 4. CarRentalSystem
- **Properties:**
  - `cars`: List of available cars.
  - `customers`: List of registered customers.
  - `rentals`: List of active rentals.

- **Methods:**
  - `addCar(Car car)`: Add a new car to the system.
  - `addCustomer(Customer customer)`: Add a new customer to the system.
  - `rentCar(Car car, Customer customer, int days)`: Rent a car to a customer for a specified number of days.
  - `returnCar(Car car)`: Return a rented car.
  - `menu()`: Display a menu for users to interact with the system.

## How to Use
1. Run the `Main` class to initialize the Car Rental System.
2. Follow the on-screen menu to rent or return cars.
3. Enter the required information as prompted.

## Sample Usage
```java
public class Main {
    public static void main(String[] args) {
        CarRentalSystem rentalSystem = new CarRentalSystem();

        Car car1 = new Car("C001", "Toyota", "Camry", 60.0);
        Car car2 = new Car("C002", "Honda", "Accord", 70.0);
        Car car3 = new Car("C003", "Mahindra", "Thar", 150.0);

        rentalSystem.addCar(car1);
        rentalSystem.addCar(car2);
        rentalSystem.addCar(car3);

        rentalSystem.menu();
    }
}


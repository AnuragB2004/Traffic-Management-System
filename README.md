# Traffic Management System

This is a simple Traffic Management System developed in C++ using file handling. The system allows for managing traffic data, including vehicles, drivers, and violations.

## Features

- Add, view, update, and delete vehicle records
- Add, view, update, and delete driver records
- Add, view, update, and delete traffic violation records
- Save and load data from files

## Getting Started

### Prerequisites

To compile and run this project, you need:

- A C++ compiler (e.g., GCC, Clang, MSVC)
- A text editor or IDE (e.g., Visual Studio Code, CLion, Code::Blocks)

### Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/your-username/traffic-management-system.git
    ```
2. Navigate to the project directory:
    ```sh
    cd traffic-management-system
    ```

### Compilation

Compile the project using a C++ compiler. For example, with g++:
```sh
g++ main.cpp -o traffic_management_system
```

### Usage

Run the compiled executable:
```sh
./traffic_management_system
```

## Project Structure

- `main.cpp`: The main entry point of the program.
- `vehicle.h` / `vehicle.cpp`: Contains the `Vehicle` class and its methods.
- `driver.h` / `driver.cpp`: Contains the `Driver` class and its methods.
- `violation.h` / `violation.cpp`: Contains the `Violation` class and its methods.
- `file_handler.h` / `file_handler.cpp`: Contains functions for file handling operations.
- `data/`: Directory to store data files.

## Classes and Methods

### Vehicle Class

```cpp
class Vehicle {
public:
    int id;
    std::string license_plate;
    std::string model;
    std::string owner;
    void addVehicle();
    void viewVehicle();
    void updateVehicle();
    void deleteVehicle();
};
```

### Driver Class

```cpp
class Driver {
public:
    int id;
    std::string name;
    std::string license_number;
    std::string address;
    void addDriver();
    void viewDriver();
    void updateDriver();
    void deleteDriver();
};
```

### Violation Class

```cpp
class Violation {
public:
    int id;
    std::string license_plate;
    std::string violation_type;
    std::string date;
    void addViolation();
    void viewViolation();
    void updateViolation();
    void deleteViolation();
};
```

### FileHandler Class

```cpp
namespace FileHandler {
    void saveVehicles(const std::vector<Vehicle>& vehicles);
    void loadVehicles(std::vector<Vehicle>& vehicles);
    void saveDrivers(const std::vector<Driver>& drivers);
    void loadDrivers(std::vector<Driver>& drivers);
    void saveViolations(const std::vector<Violation>& violations);
    void loadViolations(std::vector<Violation>& violations);
}
```

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [Anurag Bhattacharjee](https://github.com/AnuragB2004) - Initial work

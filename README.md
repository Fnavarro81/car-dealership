# Dealership Inventory Management System

A Java console application for viewing, filtering, adding, and removing vehicle inventory with pipe-delimited file persistence.

## Features
- Search vehicles by price range (`BigDecimal`), make/model, year range, color, mileage/odometer range, or vehicle type
- Display matching or full inventory records in a formatted console table
- Add new vehicles and remove existing vehicles by VIN
- Save inventory updates back to disk after adding or removing a vehicle
- Line-based input validation for menu selections (`0`–`9`), integers, and decimal prices

## Project Structure
- `Program` — entry point (`main`) that creates `UserInterface` and calls `display()`
- `UserInterface` — console menu, `promptForInt` / `promptForBigDecimal` input helpers, search/add/remove handlers, and `printDealershipTable`
- `Dealership` — stores dealership metadata (`name`, `address`, `phone`) and `inventory` (`ArrayList<Vehicle>`), with filtering, `addVehicle`, and `removeVehicle`
- `DealershipFileManager` — reads and writes dealership and vehicle records via `getDealership()` and `saveDealership(Dealership)`
- `Vehicle` — entity class with `vin`, `year`, `odometer`, `make`, `model`, `color`, `type`, and `price` (`BigDecimal`), plus getters and setters
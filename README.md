# Vehicle Information Repository

This repository contains a structured JSON file with detailed information about various vehicles, categorized by type, brand, and model.

## Table of Contents
- [Introduction](#introduction)
- [Example Usage in Python](#example-usage-in-python)
- [Example Usage in PHP](#example-usage-in-php)
- [Contribution](#contribution)
- [Give it a Star ⭐](#give-it-a-star-)

## Introduction

The purpose of this repository is to provide a comprehensive collection of vehicle information in a JSON format.

# Example Usage in Python:

```python
import json

with open('vehicles.json', 'r') as file:
    vehicle_data = json.load(file)
```

# Example Usage in PHP:

```php
<?php

$jsonFilePath = 'vehicles.json';
$vehicleData = json_decode(file_get_contents($jsonFilePath), true);
?>
```
## Using with json iterator
Since the json file is large, you can use the json iterator, which is a more performant approach; this especially prevents the max allowed memory error.

[The library](https://github.com/halaxa/json-machine)
```php
use JsonMachine\JsonMachine;

$jsonFilePath = 'vehicles.json';
$jsonMachine = JsonMachine::fromFile($jsonFilePath);
foreach ($jsonMachine as $key => $vehicle) {
   echo $vehicle->category;
   echo $vehicle->brand;
   echo $vehicle->model;
}

```
# Contribution

If you find missing or inaccurate information, contributions are welcome! Fork the repository, make your changes, and submit a pull request. Please follow the existing structure to maintain consistency.

# Give it a Star ⭐

If you find this repository useful, please consider giving it a star. It helps to increase visibility and encourages further development.

# Dynamic Tableau temporal parameters

This project is about creating a Tableau Extension which could automatically reset parameters to be at the current month.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. 

### Prerequisites

What things you need to install the extension

```
Node.js, npm
```

Integrate the .trex extension into a Tableau Dashboard with 2 integer parameters : Month and Year
Year parameter can be allowed any value, Month values between 1 and 12 with Aliases like 
"January", "February", "March", "April", "May", "June", "July", "August", "September", "October", "November", "December"

# Project setup

### Installing

Change the url in dynamicParameter.trex to localhost:8080
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

## Built With

* [Vue](https://vuejs.org/) - The web framework used
* [Tableau Extensions](https://tableau.github.io/extensions-api/) - The extension API from Tableau

## Authors

* **Julien Godenir** - *Initial work* - [Datapony](https://datapony.co)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

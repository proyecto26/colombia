# Departamentos y Municipios de Colombia

Data extracted from [Departamento Administrativo Nacional de Estadística](https://www.datos.gov.co/Mapas-Nacionales/Departamentos-y-municipios-de-Colombia/xdk5-pm3f).

## Info
- Entity name: Ministerio de Tecnologías de La Información y Las Comunicaciones (MinTIC).
- Date: 2017-05-11

## JSON Data

- Departments: https://github.com/proyecto26/colombia/raw/master/departments.json
- Cities: https://github.com/proyecto26/colombia/raw/master/cities.json

## SQL Tables

- Departments
```sql
CREATE TABLE IF NOT EXISTS department (
  id INT PRIMARY KEY,
  `name` VARCHAR(80) NOT NULL
);
```

- Cities
```sql
CREATE TABLE IF NOT EXISTS city (
  id INT PRIMARY KEY,
  `name` VARCHAR(50) NOT NULL,
  `departmentId` INT NOT NULL,
  CONSTRAINT `fk_city_department`
    FOREIGN KEY (`departmentId`)
    REFERENCES `department` (`id`)
    ON DELETE NO ACTION
    ON UPDATE NO ACTION
);
```

## Supporting 🍻
I believe in Unicorns 🦄
Support [me](http://www.paypal.me/jdnichollsc/2), if you do too.

Donate **Ethereum**, **ADA**, **BNB**, **SHIBA**, **USDT**, **DOGE**:

![Wallet address](https://user-images.githubusercontent.com/2154886/123501719-84bf1900-d60c-11eb-882c-98a499cea323.png)

> Wallet address: 0x3F9fA8021B43ACe578C2352861Cf335449F33427

Please let us know your contributions! 🙏

## Happy coding 💯
Made with ❤️

<img width="150px" src="https://avatars0.githubusercontent.com/u/28855608?s=200&v=4" align="right">

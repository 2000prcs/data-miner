# Company Data Miner
> Command Line Tool for querying company data

## Table of Contents

1. [Design Overview](#design-overview)
2. [Install Instructions](#install-instructions)
3. [Assumptions](#assumptions)
4. [Testing](#testing)
5. [Future Improvements](#future-improvements)

## Demo

<img width="400" height="300" src="https://i.imgur.com/NmPzAa9.png">


## Achievements

1. Modularized code
2. Utilized modern ES6 JavaScript formatting
3. Exhaustive tests to check result and errors

## Requirements

To run the program and run tests, Node.js must be installed in your device. 
This program is built with Node version 8.11.1

## Design overview

1. Language: I chose JavaScript with Node.js environment 
2. Main Process: Main function `miner()` takes input from STDIN => Read the file to parse data => pass the data and user query to command handlers
=> `logCompanies()` funtion takes the mapped result and log the result as string on console
3. Testing: I set up testing environment to handle testing separately. 

## Install instructions

From the root directory:

1. Install project dependencies (for testing):

```sh
npm install
```

2. Make command-line script executable:

```sh
chmod +x index.js 
```

3. Run command in the format 

For Mac OS or Linux:

```sh
./index.js [file] [command] [argument]
```

```sh
./index.js data.json find_companies_between_size 1,001-5,000
Company Names:
Abt Associates, Bridgewater, Chemical Abstracts Service, College Board, CoreLogic, Dun & Bradstreet, Esri, Fitch, Forrester Research, Gallup, Graebel Van Lines, Informatica, Inovalon, JJ Keller, Moody\'s, Morningstar, Inc., Navico

Number of Companies: 17
```

For Windows:

```sh
node.cmd index.js [file] [command] [argument]
```

## Assumptions

- I initially considered saving the data in a database, but switched my decision to go with simple JavaScript handlers. Given the fact that the amount of data is not that large, quering with the JSON file directly would be much simpler and faster.
- I was handling the commands with Switch statement in main file `index.js` originally, but separated the logic to `commands.js` for more modularization.
- My assumption is the file will be <b>JSON format</b> as mentioned in the challenge instructions. Therefore, I implemented my logic and tests with the given assumption.

## Testing

Unit tests are implemented with Jest. Testing environment is set to node.

```sh
npm test
```

## Future Improvements

- To make the program more user friendly, I can add more helpers for command or query errors. For example, I can add friendly intro giving introduction of the program or instruction when user makes an input error.
- 


## Built With

* [NPM](https://www.npmjs.com)
* [Jest](https://jestjs.io)
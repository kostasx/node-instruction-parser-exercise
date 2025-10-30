# Exercise: Instruction Parser in Node.js

## Practice Node.js async file and network methods

## Instructions:

Write a Node.js program that reads the INSTRUCTIONS.csv file,
parses the commands found within and executes them accordingly.

The CSV file contains a header line (INSTRUCTION, FILE). This should be disregarded by the Node.js 'reader'. 

The program should read each line, display a message on the screen about the instruction it is about to execute and execute the appropriate logic.

For example, for the 1st command, the console should log:

`Running instruction "Write current date"...`

Each instruction includes a filename (date.txt, jokes.txt, etc.) that must be created and filled in with some data.

For example, for the "Write current date", a new file named `date.txt` must be created and the current date in HH:MM:SS, DD/MM/YYYY format must be appended to the file.

The 'Get weather' command should reach out to a free Weather API to get the current weather for a specific city and write that data to the `weather.txt` file.

For the 'Get country' command, the code should reach out to the `https://restcountries.com/v3.1/name/greece` API endpoint based on the `data:greece` part of the instruction. If the instruction changes to `data:bulgaria` the API endpoint should change accordingly: `https://restcountries.com/v3.1/name/bulgaria`. Country data that should be written to `country.txt` should include: capital, area, population and location of capital city.

For 'Get Jokes' the following api should be used to write a joke to the `jokes.txt`: `https://v2.jokeapi.dev/joke/Programming`

- You should NOT use any sync methods! For example `fs.readFileSync`, `fs.writeFileSync`, etc.

- Try removing lines of instructions from the CSV or changing their order and ensuring that the reader still parses and executes the CSV instructions as expected.

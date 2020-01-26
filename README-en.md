# Colaborabot

### The robot created by [Colaboradados](https://colaboradados.com.br/) to monitor access to governmental public transparency portals.


<a href="https://twitter.com/colaboradados"> <img src="colaboradados_twitter_logo.png" width="200"></a>

This repository refers to our bot that monitors governmental public transparency portals. Access and follow it [**here**](https://twitter.com/colabora_bot).

## Stack

- [Python3][https://www.python.org/] the programming language needed to run the bot.
- [Virtualenv][https://docs.python-guide.org/dev/virtualenvs/] a virtual environment to isolate the packages that will be installed with the bot.

## Installing the bot

### Run locally

1. Fork the [repository](https://github.com/colaboradados/colabora_bot) to your Github.
2. Clone the repository by typing `$ git clone https://github.com/<your_github_username>/colabora_bot.git` in the terminal.
3. Activate your virtual environment and enter the bot's root folder.
4. Create a file at the root of the project called `.env`, which will be used to save the bot's configuration variables, such as tokens.
5. Copy the contents of the file `.env.example` to the newly created file `.env`.
> Note that this example file contains the variable `DEBUG=True`, which will disable the bot's external dependencies to run locally without problems.
6. Install necessary dependencies with `pip install -r requirements.txt`.
7. To run the bot, run the command `python colaborabot.py`.
8. Okay, now just run and contribute!

### Configuring external dependencies and tokens
For more details on external dependencies, visit [the integrations file here](/docs/INTEGRACOES.md).

### Collaborating with the bot (and being a very nice person)

**Colaboradados** is a nonprofit initiative made by the community with the help of it. To help with our database you can solve our issues or directly edit our file [`lista_portais.csv`](/data/lista_portais.csv).

Please be aware that our program was created with the Brazilian national scope in mind, so its code is - and should be - always in Portuguese, where possible. Avoid foreignness and collaborate so that our code is studied by all people interested in transparency.

Our project is a gateway for people from various fields to be interested in the participatory techno-civic process, therefore we believe that the bot should be easy to understand for those who are not familiar with more advanced programming techniques.

_Simple is better than complex_

_Complex is better than complicated_

## Credits

This bot was developed by [João Ernane](https://github.com/jovemadulto), [João Purger](https://github.com/JCPurger) and [Judite Cypreste](https://juditecypreste.github.io).

## The MIT License (MIT)

Copyright (c) 2019 Judite Cypreste

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

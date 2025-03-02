# Eopsin example contract

This is a sample repository to get you started with compiling your own smart contract with eopsin in less than 10 minutes (even less if you have python3.8 already installed!).
It requires you to know how to use the terminal on your computer ([Ubuntu and other Linux distributions](https://www.freecodecamp.org/news/command-line-for-beginners/), [Windows](https://www.makeuseof.com/tag/a-beginners-guide-to-the-windows-command-line/), [Mac](https://support.apple.com/guide/terminal/execute-commands-and-run-tools-apdb66b5242-0d18-49fc-9c47-a2498b7c91d5/mac)).
You should also have `git` installed.

## Installation

#### TL;DR

```bash
$ git clone https://github.com/ImperatorLang/eopsin-example.git
$ cd eopsin-example
$ python3.8 -m venv venv
$ pip install -r requirements
```

Done! If you have no clue what happened here, feel free to read the next section, which explains it step for step.
Otherwise, skip to [Running](#Running)

#### Install Python

Make sure you have `python3.8` installed.
If you don't have it installed, follow [this tutorial](https://www.geeksforgeeks.org/download-and-install-python-3-latest-version/) or just google for it.
Python is the second most used language on GitHub, there are tons of tutorials on how to use it.

#### Clone the repository

Once you have installed python, clone this repository.
Open your terminal and navigate to a folder, then run

```
$ git clone https://github.com/ImperatorLang/eopsin-example.git
```

This copies this repository on your local computer.
If you want to modify the code and keep your modifications, [fork the repository first](https://docs.github.com/en/get-started/quickstart/fork-a-repo), then clone the fork instead.

Then navigate into the the repository using the CLI, like this

```
$ cd eopsin-example
```

#### Setup the environment

This project uses the specific version of python 3.8.
For this reason we want to make sure that only this version is used for all operations.
A common way to establish that i.e. `python` also refers to `python3.8` is to set up a virtual environment.

```
$ python3.8 -m venv venv
$ source venv/bin/activate
```

You are now in a so called virtual environment.
Make sure to run the `source` command everytime you enter this repository to work on the contract,
or configure your IDE to use the created virtual environment.
When operations require you to be inside the environment, commands are prefixed with `(venv)`.

#### Install eopsin

We're almost done.
As the final step, we install the compiler, `eopsin-lang`.
We can simply use `pip` for this.
We install all projects listed in `requirements.txt`, which includes `eopsin-lang`.
If you want to use other tools as well, you can add them there!

```bash
(venv) $ pip install -r requirements.txt
```


## Running

The main code for the smart contract is located in `src`.
You can build the contract with eopsin in a single command:

```bash
(venv) $ # builds the example contract
(venv) $ eopsin build src/if_lovelace_paid_minting_policy.py "{\"constructor\": 0, \"fields\":[{\"bytes\": \"abf5de8ba711a8f9889a5b7865d8c1eefb72a06280c7a5a11bc4a571\"}, {\"int\":4000000}, {\"bytes\":\"4d656d62657273686970\"}]}"
```

# Interview task

## Overview
In this task, I would like you to conduct a small research project entirely from scratch. It will be representative of the work we will do. To mimic reality, it is both *open-ended* and *idealized* - you may well find unexpected difficulties along the way.

## Task
Please construct a simple
[momentum](https://en.wikipedia.org/wiki/Momentum_(technical_analysis))
signal on the
[S&P100](https://en.wikipedia.org/wiki/S%26P_100).
You may use any value of `N`.
We will use:

- [yfinance](https://github.com/ranaroussi/yfinance) to the fetch the data,
- [pandas](https://github.com/pandas-dev/pandas) to organize and analyze it, and
- [jupyter lab](https://github.com/jupyterlab/jupyterlab/) to present it.
- any visualization library of your choice.

Assemble the data for any 5-year period. For simplicity, you may assume that the universe over that period of time is constant with the same constituents as those in the S&P today.

Let `0.0 < f < 0.5` and `r >= 1` be parameters. We will hold:

- $1 in each of the top `f` fraction of names (e.g. if `f = 0.1`, then we will long each of the top 10% of names), and
- -$1 in each of the bottom `f` fraction of names.
  
We will rebalance every `r` days.

Please plot the cumulative PnL according to a handful (say 2-3) combinations of `f` and `r`. Compute any additional portfolio statistics you wish to discuss.

You are, of course, allowed to GitHub/StackOverflow/etc for any help you might need.

## Setup
You must use:

- this current Windows machine.
- [GitHub](https://github.com/) to host the code.
  
To set GitHub up:

- Log into [GitHub](https://github.com/) as `derekwanclsa`.
- Create a new private repo with your name:
- Use `git bash` to clone the repo:
  
  ![...](doc/git-bash.png)

Everyone as their own development environment. You are welcome to go and configure your own, but only the end result will be considered. As time is limited, this may well be infeasible. Hence, the following are also provided:

- [conda](https://docs.conda.io/en/latest/), a Python environment manager.
- [PyCharm](https://www.jetbrains.com/pycharm/), a Python IDE.

You are not expected to be familiar with them, so you will be walked through their configuration. First, we set up `conda`:

- Start `anaconda powershell prompt`:
  
  ![...](doc/anaconda-prompt.png)
  
- Navigate to your repo and run `conda env create --force`:
  
  ![...](doc/installing-conda.png)
  
  After a minute or two:
  
  ![...](doc/installing-conda2.png)
  
- If you wish to add packages:
  - Add them to `environment.yml`:
    
    ![...](doc/adding-to-environment.png)
    
  - Then run `conda activate  `conda env update`:
    
    ![...](doc/adding-to-environment2.png)
    
Next, we set up PyCharm:

- Go to the "Settings":
  
  ![...](doc/pycharm-interpreter.png)
  
- Go to "Project Interpreter" and show all:
  
  ![...](doc/pycharm-interpreter2.png)

- Go to add:
  
  ![...](doc/pycharm-interpreter3.png)

- Go to "Conda Environment" > "Existing environment" and then expand the list of interpreters:
  
  ![...](doc/pycharm-interpreter4.png)

- Select `python3.exe` under the `miniconda3` folder:
  
  ![...](doc/pycharm-interpreter5.png)

- Double check you have added the environment correctly:
  
  ![...](doc/pycharm-interpreter6.png)

- PyCharm should now be linked to the environment, providing auto-completions et al:
  
  ![...](doc/pycharm-auto-completion.png)

### PyCharm




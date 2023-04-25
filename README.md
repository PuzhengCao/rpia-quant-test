# Summary

You are being required to build a portfolio optimizer for a client, to replicate an index of bonds.

The bonds are assumed to be denominated in the same currency so no FX needs to be considered.

The bonds are all fixed rate and pays interest semi-annually, with price quoted in terms of 100.

The bonds are assumed to be non-callable, and no crediut risk is considered.

# Data

The index is composed of all bonds found in the `security.csv` file.

Their holdings everyday is found in the `holdings.csv` file.

The daily pricing metrics are found in the `metrics.csv` file.

All three files are in the `data` folder.

# Question

1. Build an optimizer that can generate an optimized portfolio with a goal to replicate the index's performance and risk profile as of snapshot of a day .

   - The client wants to match the index's duration profile by certain buckets.

     - Use your best judgement to determine what are the tenor buckets that should be considered in this case.
     - Design a mechnism to reallocate the IR exposure into these tenors.
     - If you can justify your decision quantitatively, that would be even better.

   - For this question, you can use outright duration matching.

     - Keyrate duration matching and convexity matching are more advanced topics, and are not required for this task.
     - It will be a bonus if you can implement them as well.

   - The client is concerned about underperformance vs the index, but not outperformance.
     - So in an ideal scenario, your portfolio should return slightly higher than the index, but not lower.

1. Generate some basic visualization to compare the optimized portfolio vs the index.

1. Generate daily rebalancing trades based on the index changes.

   - You can assume all trades are executed at the end of the day at the closing price, so no slippage is incurred.
   - Explain the logic behind your rebalancing strategy, any data issue you have encountered, and how you ended up solving them.

1. Test your optimizer by measuring the performance of your constructed portfolio vs the index daily. Explain the results on a high level.

1. Any other ideas you can think of to improve the optimizer? It can be only theoretical.

1. Structure your code and repos in a way that it can be easily maintained and scaled.

   - You can assume that the optimizer is only one of the first steps in a long-term project, and it will be used as a module in a larger system.
   - Describe on a high level how you would improve the code structure and workflow if you have more time, for example, data pipeline, testing, etc.

# Guidelines

1. Programming language: strongly preferred **Python/Jupyter Notebook**.

1. The questions are on a best-effort basis. Focus more on your thought process and the quality of your work, rather than the quantity.

1. Necessary comments should be in the code, and documentation in the form of a `README.md` and a `setup.md` file, if applicable.

1. You are free to use any libraries or packages that you deem necessary, but a clear explanation of why you chose to use them, and what the package is doing for you should be included in the `README.md` file.

   Hint: For the optimization part, you could consider using `cvxpy`.

1. You are free to use any online coding support platform (including ChatGPT), but you should be able to explain the code you wrote.

# Deliverables

1. Please **do not fork** the repo (unless you want to share your work with others).

   Instead, pull the repo to your local machine, and create a new remote repo on your own GitHub account.

   Once you are done, send it to _rcao@rpia.ca_ or invite _PuzhengCao_ to your repo.

1. You will be given access to the repo at 5:00 pm EST on Friday, April 28th, and you will have until 9:00 am EST on Monday, May 1st to complete the task.

   Any commits after the deadline will not be considered.

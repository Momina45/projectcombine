 Bill Splitter Application
-Introduction
   The Bill Splitter application helps users manage and split bills among friends,
   calculating each person's balance based on their participation in group expenses.
   It is useful in social settings like dining out where shared expenses need to be fairly split
-My contribution
   1. addFriend(string &name)
This method adds a friend to the balances data structure, where each friend’s balance starts at 0.
If the friend is already present, a message is displayed stating that the friend is already added.

Parameters:
name: The name of the friend to be added to the balance sheet.
Functionality:
If the friend does not exist in the unordered_map balances, they are added with an initial balance of 0.
If the friend is already present, a message will be shown: "name is already added"

   2. addExpense(string &payer, vector<string> &payees, double amount)
This method records an expense, with one payer and multiple payees. It updates the payer's balance by the total amount and deducts the respective share from each payee's balance.

Parameters:

payer: The name of the friend who paid for the expense.
payees: A vector of friends who are sharing the expense.
amount: The total amount of the expense.
Functionality:

The method first checks if the payer exists in the balances. If not, it displays an error message: "Payer not found."
The expense is divided equally among all payees, and the payer's balance is increased by the total expense.
Each payee's balance is decreased by their share of the expense.
If a payee does not exist in the balances, an error message is displayed: "Payee not found."

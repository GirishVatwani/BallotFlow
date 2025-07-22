# 🎲 BallotFlow: A Ranked-choice Voting Simulator

Welcome to **BallotFlow**, an interactive simulation of the ranked-choice (runoff) voting system, built as part of the CS50 curriculum. This project emulates how real-world runoff elections are held: if no candidate wins a majority of votes, the least popular candidates are gradually eliminated and votes are redistributed based on voter preference until a winner is determined.

---

## 🚀 How It Works

1. **Voters rank candidates:** Each voter lists their candidate preferences in order (1st, 2nd, 3rd, ...).
2. **Votes are tallied:** If any candidate has a majority (>50%) of votes in the current round, they are declared the winner.
3. **Elimination:** If no candidate has a majority, the candidate(s) with the fewest votes are eliminated.
4. **Redistribution:** Voters who selected eliminated candidates as their top choice have their votes transferred to their next highest-preferred non-eliminated candidate.
5. **Repeat:** Steps 2-4 are repeated until a winner is found or a tie occurs.


---

## 📝 Example Scenario

Suppose there are **three candidates**: Alice, Bob, and Charlie.<br>
**5 voters** rank their preferences as follows:

| Voter | 1st Choice | 2nd Choice | 3rd Choice |
|-------|------------|------------|------------|
| 1     | Alice      | Charlie    | Bob        |
| 2     | Bob        | Charlie    | Alice      |
| 3     | Charlie    | Alice      | Bob        |
| 4     | Charlie    | Bob        | Alice      |
| 5     | Bob        | Alice      | Charlie    |

#### **First Round:**
- Alice: 1 vote
- Bob: 2 votes
- Charlie: 2 votes

No one has more than half the votes (3 out of 5), so **Alice is eliminated**.

#### **Second Round (redistribute Alice's vote):**
- Bob: 2 votes
- Charlie: 3 votes

**Charlie wins!**



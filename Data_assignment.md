# FIFA World Cup Analysis – Sum of Goals Scored by Winner

## Objective
To analyze the **sum of goals scored (`goals_scored`) by each FIFA World Cup winning team (`winner`)** across all FIFA World Cup tournaments. This analysis helps compare the overall goal-scoring performance of World Cup champions.

---

## Source
- **Dataset:** FIFA World Cup Dataset
- **Source:** Kaggle

---

## Data Collection Method
The data was collected from the **FIFA World Cup dataset available on Kaggle**. The dataset contains historical information about FIFA World Cup tournaments, including:

- Tournament Year
- Host Country
- Winner
- Runner-up
- Goals Scored
- Matches Played
- Qualified Teams
- Attendance

For this analysis:
- The **Winner** and **Goals Scored** columns were selected.
- A **Pivot Table** was created in Microsoft Excel.
- The **Sum** aggregation function was applied to the `goals_scored` field and grouped by the `winner` field.

---

## Data Presentation
The processed data is presented using:

- **Pivot Table** to summarize the total goals scored by each World Cup-winning nation.
- **Bar Chart** to visually compare the cumulative goals scored by different FIFA World Cup champions.

### Summary of Results

| Winner | Sum of Goals Scored |
|---------|--------------------:|
| Brazil | 612 |
| Italy | 447 |
| West Germany | 352 |
| France | 340 |
| Argentina | 234 |
| Germany | 171 |
| Uruguay | 158 |
| Spain | 145 |
| England | 89 |

---

## Graph Interpretation

The bar chart clearly illustrates the total goals scored by each FIFA World Cup-winning nation.

### Key Observations

- **Brazil** has the highest cumulative goals scored (**612**), indicating its strong attacking performance across its World Cup-winning campaigns.
- **Italy** ranks second with **447** goals.
- **West Germany** and **France** follow with **352** and **340** goals, respectively.
- **Argentina** has accumulated **234** goals.
- **Germany**, **Uruguay**, and **Spain** have moderate totals.
- **England** has the lowest cumulative goals (**89**) among the winning nations shown.

---

## Conclusion

The analysis demonstrates that **Brazil** is the most dominant World Cup-winning nation in terms of cumulative goals scored. Using **Microsoft Excel Pivot Tables** and **Bar Charts** makes it easy to summarize, compare, and visualize the performance of FIFA World Cup champions based on total goals scored.
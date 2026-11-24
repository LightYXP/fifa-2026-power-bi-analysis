# FIFA 2026 | Player Performance Analysis

An exploratory Power BI portfolio project comparing football player performance by team, position and month. Results illustrate the supplied dataset and are not verified official tournament statistics.

## Report pages

| Page | Features |
| --- | --- |
| Team | Team and position slicers; goals, assists, average rating and pass accuracy KPIs; player rating and goal/assist comparisons. |
| Player | Team, position and player slicers; goals, assists, shot conversion, average rating and monthly performance trends. |

## Tools and techniques

- Microsoft Power BI Desktop
- DAX measures and filter context
- KPI cards, slicers, bar and column charts, line charts
- Monthly aggregation and custom report theme

## Key measures

```dax
Shot Conversion % = DIVIDE(SUM('fifa_world_cup_2026_player_performance'[goals]), SUM('fifa_world_cup_2026_player_performance'[shots]), 0) * 100

Average Rating = AVERAGE('fifa_world_cup_2026_player_performance'[player_rating])

Pass accuracy % = AVERAGE('fifa_world_cup_2026_player_performance'[pass_accuracy]) * 100
```

Pass accuracy is an unweighted average of recorded accuracy values. Shot conversion is aggregate goals divided by aggregate shots.

## Project status

The report contains two pages and 20 visual objects. Archive integrity and visual definitions were inspected; full execution has not been tested. Dashboard files and screenshots are pending publication. The original dataset source and redistribution license remain unverified. Before release, validate the Top N rating filter and player slicer selection behavior.

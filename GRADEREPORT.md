# Grading Report

**Final Grade: 5.5/10.00**

## Rubric

| Criterion | Points |
|-----------|--------|
| `extract_data` correctly slices, title-cases names, int conversion, extracts grades, and leaves input untouched | **1.5** |
| `curve_grades` applies the curve (while loop) and caps values at 100 | **0** |
| `print_top_performers` prints only qualifying `Name: Score` lines (>= 95) | **3** |
| Code quality (required loop choices, clear logic) | **1** |


## General Comments

I can see that you undestand the materials but got hung-up on the first function. Maybe you tried to overcomplicate things.

The main issue in extract_data is this:

You overwrite s_names and s_grades each loop, instead of appending to them.
So at the end of the loop, you only return the last record.

Also, popping both items from the same list modifies the raw_data.



## Functionality

- tests/test_grader.py::RosterHelperTests::test_curve_grades_values_and_clamping: Failed (0.0 points)

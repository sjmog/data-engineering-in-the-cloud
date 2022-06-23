# Specification: Early Education and Belonging

How crucial are those early years of education on social wellbeing? How does the number of years in early education impact a student's sense of belonging?

Here's the sort of thing we're aiming for:

![A bubble chart of Early Education and Belonging, with the bubbles related to the number of submissions in each country](../../images/early_education_and_belonging.png)

## Data structure

This chart expects the following sort of data structure:

```json
{
  "dataset": [
    // one of the below object for each country
    {
      "id": "A three-letter country code, uppercased. e.g. GBR",
      "data": [
                {
                  "x": "DURECEC as an integer, e.g. 6",
                  "y": "BELONG as a float, e.g. 1.1",
                  "submissions": "a count of submissions from this country as an integer, e.g. 412"
                }
              ]
    }
  ]
}
```

## Statistical analysis

This chart is made up of two computed indices: the number of years in early education (`DURECEC`) and an index of belonging (`BELONG`).

To construct them, consult the [PISA 2018 Annex A1](https://www.oecd-ilibrary.org/sites/84a683c1-en/index.html?itemId=/content/component/84a683c1-en#sect-106).

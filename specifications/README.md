# Specifications

This directory contains instructions for how to make the Forage charts work.

Each chart has the following:

1. An expected data structure.
2. Some statistics to get correct values for the data structure.

## Expected data structure

The expected data structure will determine what learners return from the endpoints through which they expose their data.

Forage charts poll a learner-configured endpoint every second. The charts expect to receive a particular JSON data structure, which they'll then plot.

Some charts also send query parameters to the endpoints.

The specification lists the expected data structure and any queries that might be sent.

## Statistics

Some charts are quite simple – for instance, counts of data. Some are more complex, requiring columns to be averaged or standardised to yield an index. Some are yet more complex, requiring the combination of several different computed indices.

Each specification contains information about how to construct the values that input to the eventual dataset.

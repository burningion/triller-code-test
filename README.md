# Triller Backend Code Test

## Traveling Salesmen As A Service

You've been given the task to build an API that solves the traveling
salesman problem, and returns the optimal route via JSON. You must use
simulated annealing to implement the search for the sortest route.

The data sent to the API looks like the following:

```json
{
"Charlotte": [35.23, 80.85],
"San Francisco": [37.78, 122.42],
"Houston": [29.77, 95.33],
"Columbus": [39.98, 82.98],
"Detroit": [42.33, 83.05],
"Phoenix": [33.45, 112.07],
"Los Angeles": [34.05, 118.25],
"New York City": [40.72, 74.0],
"San Diego": [32.78, 117.15],
"Memphis": [35.12, 89.97],
"Baltimore": [39.28, 76.62],
"San Antonio": [29.53, 98.47],
"Fort Worth": [32.75, 97.33],
"Jacksonville": [30.32, 81.7],
"San Jose": [37.3, 121.87],
"Philadelphia": [39.95, 75.17],
"Dallas": [32.78, 96.8],
"Chicago": [41.88, 87.63],
"Indianapolis": [39.78, 86.15],
"Austin": [30.27, 97.77]
}
```

Your API will have an endpoint, /anneal, and when posted to via JSON
formatted as above, will return results with the optimal (shortest)
route between places (for a dataset with < 50 places).

Here's a possible example for what requesting the API might look like
from the command line. You'll notice our anneal.json file has been
included with this repository:

```bash
$ curl -H 'Content-Type: application/json' --data @anneal.json localhost:5000/anneal
{
"items": [
"New York City",
"Philadelphia",
"Detroit",
"Columbus",
"Indianapolis",
"Chicago",
"Memphis",
"Dallas",
"Fort Worth",
"Phoenix",
"Los Angeles",
"San Francisco",
"San Jose",
"San Diego",
"Austin",
"San Antonio",
"Houston",
"Jacksonville",
"Charlotte",
"Baltimore"
]
}
```

## Requirements

You can write the code in any language you choose. You should aim to
have something up and running in under two hours that passes the
previous test, and matches the output. We don't expect perfection, and
you're free to use any libraries you need.

You should also familiarize yourself with the traveling salesman
problem, and should be able to describe how simulated annealing works,
and have some ideas for potential problems that we might experience,
if we deployed this code to the wild.

Send us your code attached to an email along with instructions for
running your code. And thanks!


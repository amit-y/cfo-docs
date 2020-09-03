# Cards for Observability

Cards for Observability is a programmable dashboard app for deployment in [New
Relic One](https://newrelic.com/platform). In order to create a dashboard in the
app, you need to be familiar with a few concepts.

## Cards

Cards are the visual representation of the data. You can have one or more cards
on a dashboard. You control what appears on a card by providing the HTML and CSS
for each card.

## Queries

Queries are more than just New Relic queries in NRQL (New Relic Query Language).
Queries can be NRQL or GraphQL. In addition, queries can have one or more steps
they flow through. Here's a simple example of a flow...

1. GraphQL query returns a list of services and its health
2. For each service, a NRQL query returns the health of the host on which the service is running

In addition to being a query, a step could also...

1. Make HTTP requests (like API calls)
2. Parse the result using javascript
3. Be a map function
4. Be a reduce function

## Scripts

Scripts are free form javascript you can execute when a dashboard loads. You can
also load external javascript libraries.

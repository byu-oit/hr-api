# Employees API

The Employees UAPI is run on the back-end by PeopleSoft, which leaves it with some technical quirks that may cause some inconveniences to subscribers.

## Query Parameters
Because of these limitations, if there are query parameters in the url, they **_must_** be specified in _exactly_ the order that the API specifies. Where applicable, the swagger for the Employees API will indicate which paramters are allowed in which path, and what order they need to be specified in.

If you fail to specify the query parameters in the order that PeopleSoft needs, you may get an generic 500 error with no response body.

## JWT and sm_user
Currently, PeopleSoft doesn't support JWT for authentication. This is under development, so this may change in the future. For now, it requires that the sm_user be set to the net id of the authenticated user. In WSO2, this is done automatically by adding the `AddCFrameworkHeaders` to the `In Flow` option in the `Message Mediation Policies` when the API is set up, so this shouldn't be a concern for most subscribers.

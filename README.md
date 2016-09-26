# as-eid-inj
Basic setup for reproducing the XSS issue via the `eid` param in ActiveScaffold.

Set everything up, seed the DB, then launch the app and access the following URL: http://localhost:3000/users?eid=1%22%20onmouseover%3dprompt%28%22XSS!%22%29%20bad%3d%22 .

That should lead to the JS code being injected and executed on the corresponding event.

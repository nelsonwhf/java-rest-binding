The Java binding for the Neo4j Server REST API wraps the REST calls behind the well known
[GraphDatabaseService](http://api.neo4j.org/1.2/org/neo4j/graphdb/GraphDatabaseService.html) API.

Currently supports:
* all the node and relationship operations
* the new Index API
* Basic Http Auth (Digest)
* preliminary traversal support

Open issues:
* full traversal support
* support for exposing server extensions - via an interface based proxy

Usage:

<pre>
GraphDatabaseService gds = new RestGraphDatabase(new URI("http://localhost:7474/db/data"));
GraphDatabaseService gds = new RestGraphDatabase(new URI("http://localhost:7474/db/data"),username,password);

<bean id="graphDbService" class="org.neo4j.rest.graphdb.RestGraphDatabase" destroy-method="shutdown">
    <constructor-arg index="0" value="http://localhost:7474/db/data" />
</bean>
</pre>

Please note: Transactions are not supported over this API.

References / Community:

* [Neo4j community site](http://neo4j.org)
* [Neo4j REST API](http://components.neo4j.org/neo4j-server/milestone/rest.html)

Community:
* [Neo4j Wiki](http://wiki.neo4j.org)
* [Neo4j Mailing List](https://lists.neo4j.org/mailman/listinfo/user)
# neo4j-presentation

<pre>
create (q:Punc {name:"?"}), (g:Graph {name:"GRAPH"}) return q, g
</pre>

<pre>
create (n1:Person {name:"Tom", species:"cat", age:"not 18", phone:"0844332244", email:"DJ@satan.com"}), (n2:Person {name:"Jerry", expertise:"relationship", species:"magic mouse"})
create (c:CMS {name:"Wordpress"})
create (h:Office {name:"Exove Office", number:"2", street:"17"})
create (n1)-[:RELATES_TO {relationship:"Fellow DruPals",first_meeting:"Uranus",first_impression:"cool guy"}]->(n2)
create (n1)-[:STAYS_IN]->(h), (n2)-[:STAYS_IN]->(h)
create (n1)-[:MASTERS]->(c)
create (h)-[:MAJOR_BOSS]->(c)
return n1,n2,h
</pre>

<pre>
create (g:Graph {name:"GRAPH"}), (n:Neo {name:"NEO4J ????"}), (g)-[r:WTF]->(n) return g,n,r
</pre>

<pre>
create
  (n:Neo4j {name:"NEO4J"}),
  (g:Graph {name:"GRAPH"}),
  (i:Idea {name:"IDEA"}),
  (l:Language {name:"Java"}),
  (cy:Cypher {name:"CYPHER", definition:"Neo4j database query langue"}),
  (rest:API {name:"REST API"}),
  (libs:Libs {name:"LIBRARIES/NEO4J DRIVERS"}),
  (a:Band {name:"ABBA (THE BAND)"}),
  (c:Country {name:"SWEDEN"}),
  (js:Language {name:"JAVASCRIPT"}),
  (py:Language {name:"PYTHON"}),
  (net:Language {name:".NET"}),
  (ruby:Language {name:"RUBY"}),
  (php:Language {name:"PHP"}),
  (tr:Language {name:"R, GO, CLOJURE, PERL, HASKELL"})
create
  (n)-[:IS]->(g), (g)-[:IS]->(i),
  (n)-[:WRITTEN_IN]->(l),
  (n)-[:RELATES_TO]->(a)-[:FROM]->(c)&lt;-[:FROM]-(n),
  (n)-[:HAS]->(cy),
  (n)-[:HAS]->(rest),
  (n)-[:HAS]->(libs),
  (libs)-[:AVAILABLE_IN]->(l),
  (libs)-[:AVAILABLE_IN]->(net),
  (libs)-[:AVAILABLE_IN]->(js),
  (libs)-[:AVAILABLE_IN]->(py),
  (libs)-[:AVAILABLE_IN]->(ruby),
  (libs)-[:AVAILABLE_IN]->(php),
  (libs)-[:AVAILABLE_IN]->(tr)
foreach (x in [1,2,3,4]| create (a)&lt;-[:HATES]-(Hater {name:"Hater"})-[:HATES]->(c))
return n,g,i,l,cy,rest,libs
</pre>

<pre>
create
  (n:Neo4j {name:"NEO4J"}),
  (s1:Step {name:"brew install neo4j"}),
  (s2:Step {name:"neo4j start"}),
  (s3:Step {name:"localhost:7474"})
create
  (n)-[:FOLLOWS_BY]->(s1),
  (s1)-[:FOLLOWS_BY]->(s2),
  (s2)-[:FOLLOWS_BY]->(s3)
return n
</pre>

<pre>
optional match ()-[r1]->() delete r
</pre>

<pre>
match (n) delete n
</pre>

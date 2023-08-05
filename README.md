# poc_neo4j_docker

Instructions to follow:

1. Download neo4j docker image by command :
   docker run neo4j
2. After installing, run the following docker run command:
  docker run --name testneo4j2 -p7474:7474 -p7687:7687 -d -v "{PATH_TO_PROJECT_FILES}/data:/data" -v "{PATH_TO_PROJECT_FILES}/logs:/logs" -v "{PATH_TO_PROJECT_FILES}/import:/var/lib/neo4j/import" -v "{PATH_TO_PROJECT_FILES}/plugins:/plugins" --env NEO4J_AUTH=neo4j/password --env NEO4J_dbms_connector_https_advertised__address="localhost:7473" --env NEO4J_dbms_connector_http_advertised__address="localhost:7474" --env NEO4J_dbms_connector_bolt_advertised__address="localhost:7687" neo4j:latest

3. Once done, open neo4j browser and check if the user is connected to neo4j.

4. Run the python script to load data from csv into the graphs.

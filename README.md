# poc_neo4j_docker

Instructions to follow:

1. Download neo4j docker image by command :
   docker pull neo4j:latest

2. After installing, run the following docker run command:
  docker run \
   --name Demo_Neo4J \
   -p7474:7474 -p7687:7687 \
   -d \
   -v "D:/Users/swara/Desktop/Neo4J/TestProject/docker_files/data:/data" \
   -v "D:/Users/swara/Desktop/Neo4J/TestProject/docker_files/logs:/logs" \
   -v "D:/Users/swara/Desktop/Neo4J/TestProject/docker_files/import:/var/lib/neo4j/import" \
   -v "D:/Users/swara/Desktop/Neo4J/TestProject/docker_files/plugins:/plugins" \
   --env NEO4J_AUTH=neo4j/password \
   --env NEO4J_dbms_connector_https_advertised__address="localhost:7473" \
   --env NEO4J_dbms_connector_http_advertised__address="localhost:7474" \
   --env NEO4J_dbms_connector_bolt_advertised__address="localhost:7687" \
   neo4j:latest

4. Once done, open neo4j browser at http://localhost:7474/browser/ and check enter username password as neo4j and password respectively to connect to neo4j db.

5. Upload the csv files to path : {PATH_TO_PROJECT_FILES}/import/

6. Run the python script to load data from csv into the graphs.

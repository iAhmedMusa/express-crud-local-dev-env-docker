# Starts mongodb command
docker run -d \
-p 6677:27017 \
--network mongo_network \
--name mongodb \
-e MONGO_INITDB_ROOT_USERNAME=admin \
-e MONGO_INITDB_ROOT_PASSWORD=password \
mongo

# Starts mongo-express command
docker run -d \                                                     
-p6678:8081 \
--name mongo-ui \
-e ME_CONFIG_MONGODB_ENABLE_ADMIN=true \
-e ME_CONFIG_MONGODB_ADMINUSERNAME=admin \
-e ME_CONFIG_MONGODB_ADMINPASSWORD=password \
--net mongo_network \
-e ME_CONFIG_MONGODB_SERVER=mongodb \
mongo-express
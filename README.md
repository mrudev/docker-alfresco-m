# docker-alfresco-m

Format run command: 

docker run --name='{container_name}' -p 8080:8080 -p 7070:7070 -p 8009:8009 -p 8443:8443 -e 'DB_KIND=postgresql' -e 'DB_HOST={db_hostname}' -e 'DB_USERNAME={db_username}' -e 'DB_PASSWORD={db_password}' -e 'DB_NAME={db_name}' -e 'S3_ACCESS_KEY={s3_access_key}' -e 'S3_SECRET_KEY={s3_secret_key}' -e 'S3_BUCKET_NAME={s3_bucket_name}' --detach {image_name}


Met volumes:

docker run --name='{container_name}' -p 8080:8080 -p 7070:7070 -p 8009:8009 -p 8443:8443 -v '/host/alfresco-4.2/logs:/alfresco/tomcat/logs' -v '/host/alfresco-4.2/solr:/alfresco/alf_data/solr4' -v '/host/alfresco-4.2/contentstore.deleted:/alfresco/alf_data/contentstore.deleted' -e 'DB_KIND=postgresql' -e 'DB_HOST={db_hostname}' -e 'DB_USERNAME={db_username}' -e 'DB_PASSWORD={db_password}' -e 'DB_NAME={db_name}' -e 'S3_ACCESS_KEY={s3_access_key}' -e 'S3_SECRET_KEY={s3_secret_key}' -e 'S3_BUCKET_NAME={s3_bucket_name}' --detach {image_name}

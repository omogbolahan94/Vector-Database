# ABOUT 
Building a vector databse with elasticsearch

# STEPS
* In dicker, build the elasticsearch image and create a container by running the image:
```
docker run -it \
    --rm \
    --name elasticsearch \
    -p 9200:9200 \
    -p 9300:9300 \
    -e "discovery.type=single-node" \
    -e "xpack.security.enabled=false" \
    docker.elastic.co/elasticsearch/elasticsearch:8.4.3
```
The comand above will establish `elasticsearch` connection.
* Prepare the dataset for elastic: in this project, a JSON file.
* Embed the documents into a densed vector using a pretrained model: `SentenceTransformer` after installing it (`pipenv install sentence_transformer`).
* Confirm if `elasticsearch` is running.
* Create a mapping (meta data) and use it to create index.
* Add document into `elasticsearch` index.
* 


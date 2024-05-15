# elasticsearch-search-demo
Code solution to the Elasticsearch search [tutorial](https://www.elastic.co/search-labs/tutorials/search-tutorial/welcome)


## How to run the code
Run a single-node elasticsearch cluster and kibana using docker
```bash
> docker run --name elasticsearch01 --net elastic -p 9200:9200 -e "discovery.type=single-node" -e "xpack.security.enabled=false" -e "xpack.security.http.ssl.enabled=false" -t docker.elastic.co/elasticsearch/elasticsearch:8.13.4
```

Run the code
```bash
> cd search-tutorial
> python3 -m venv venv # create a virtual environment
> source venv/bin/activate
> pip install -r requirements.txt
> flask run
> # open the browser and navigate to `http://localhost:5001` to access the search page
```
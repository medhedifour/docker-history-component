# docker-history-component

The history contains all data related to the application and its microservices.

Our history is generated and updated at real time. 
For each number of requests, we saved cpu usage, memory usage, and response time of the container. 
For each record, we verify if it’s an outlier, if it’s the case it won’t be saved in the history, while it reflects an abnormal behavior, else it will be added. 

We base the outlier detection on modified z-scores method, a robust technique for outlier detection.

This component is based on sysdig monitor which helps to get data at real time for all layers (microservice, container, VM).

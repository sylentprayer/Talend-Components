Elasticsearch Indexing Talend Custom Component
================================================
<br/>
Often, we need full text search support in our application along with analytics. Having a component will allow indexing created/updated along with data loaded in warehouse. So, I have created a component for indexing (create/update) for Elasticsearch. Elasticsearch, is distributed, open source, full text engine built on top of Lucene. It is well documented, supports REST API over JSON and many other native language API for indexing and querying.

NOTE: To support add or update, at least one field in schema must be designated as key to identify rows as unique. Multiple columns can be designated as key (in case of composite primary keys).

Elasticsearch 1.2.0+ needs JDK 7, hence dependent jar elasticsearch<version>.jar has same dependency and need to use JDK 7 in Talend Studio.

Deploying the component
=======================
* Get component from GitHub:
	* git clone https://github.com/sylentprayer/Talend-Components.git OR clone using Github client, OR download zip from https://github.com/sylentprayer/Talend-Components
	* Get tElasticsearchIndex folder containing component.
	
* Copy tElasticsearchIndex directory (talend-components) to Talned plugin:
	* Copy tElasticsearchIndex into $TALEND_HOME/plugins/org.talend.designer.components.localprovider_*/components/

* Restart talend or press ctrl+shift+F3

See tutorial for component here http://spring-webservice-2-step-by-step.blogspot.in/2014/01/talend-elasticsearch-indexing-tutorial.html

Download example jobs from https://github.com/sylentprayer/sample-projects/releases

Alternatively you could use any of the components without using git at all. This can be downloaded as zip after official release.

I FACED LOT OF ISSUES IN TALENDFORGE SO MOVED COMPONENT TO GITHUB. TALENDFORGE THROWS ERROR WHILE ADDING COMPONENT AND I TRIED FOR TWO DAYS.

Other component tMustache hosted at http://www.talendforge.org/exchange/index.php?eid=1089&product=tos&action=view

Also need some improvement [write to me if these are useful to you]:
--------------------------------------------------------------------
* Input for multiple elasticsearch hosts (will be useful in load balancing huge data).

* Support for Elasticsearch settings, whichever applied to a transport client.

* Support for error hadling and notification in bulk indexing.

* Support for providing statistics of documents added/updated to index.

ES API reffered in this component:
http://www.elasticsearch.org/guide/en/elasticsearch/reference/current/docs-index_.html
http://www.elasticsearch.org/guide/en/elasticsearch/reference/current/modules-transport.html

Other components in pipeline:
==============================
* Cassandra support using CQL3 native binary protocol (using Datastax Java driver). 

* Other components for Elasticsearch for read operations (suggest usecases).

* Execute R script in Talend (using FastR, R interpreter written in Java).

Suggest more usecases.

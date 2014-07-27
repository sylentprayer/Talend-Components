Elasticsearch Indexing Talend Custom Component
================================================
<br/>
Talend Open Sutio is open source ETL tool, supporting 450+ components (read/writre/transorm). Support for most of the databases, file ormats and 
other data sources, like web service, FTP, SMTP and some NoSQL, HDFS/Hadoop (in Talend BigData). But, no component to work with full text search
engines like Lucene, Solr or Elasticsearch.

Often, we need full text search support in our application along with analytics. Having a component will allow indexing created/updated along with
data loaded in warehouse. So, I have created a component for indexing (create/update) for Elasticsearch. Elasticsearch, is distributed, open source,
full text engine built on top of Lucene. It is well documented, supports REST API over JSON and many other native language API for indexing and querying.

NOTE: This component is tested with Elasticsearch version 0.90.7. And, to support add or update, at least one field in schema must be designated as key to identify rows as unique. Multiple columns can be designated as key (in case of composite primary keys).

Also need some improvement:
* UI form for input and tooltips.

* Input for multiple elasticsearch hosts.

* Support for Elasticsearch settings, whichever applied to a transport client.

* Support for error hadling and notification in bulk indexing.

* Support for providing statistics of documents added/updated/deleted ti index.

Deploying the component
=======================
* Create new directory:
	* cd /tmp

* Get component from Codebreak Git:
	* git clone https://pklalitjha@git.codebreak.com/pklalitjha/talend-components.git

* Copy tElasticsearchIndex directory (talend-components) to Talned plugin:
	* cp -R /tmp/talend-components/tElasticsearchIndex $TALEND_HOME/plugins/org.talend.designer.components.localprovider_*/components/

* Restart talend or press ctrl+shift+F3

Alternatively you could use any of the components without using git at all. This can be downloaded as zip after official release.

Other components in pipeline:
==============================
* Cassandra support using CQL3 native binary protocol (using Datastax Java driver). 

* Other components for Elasticsearch for read operations (suggest usecases).

* Execute R script in Talend (using FastR, R interpreter written in Java).

Suggest more usecases.
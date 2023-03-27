<style>
  .md-content__button {
    display: none;
  }
</style>
# Data Resource Fields




The metadata specification for a DIGITbrain Data Resource
has these fields:

`kind`{ #kind }

:   **Optional**-*List[DATA_KIND]*- supported types of the data resource (e.g. file/object storage, database management system, streaming broker). FILE can mean a single file or a folder.


    === "Example"
        ``` yaml     
        ["FILE", "STREAM"]
        ```

`direction`{ #direction }

:   **Optional**-*List[DATA_DIRECTION]*- supported direction of data flow (source: data provider, sink: data consumer/storage)


    === "Example"
        ``` yaml     
        ["SOURCE", "BIDIRECTIONAL"]
        ```

`format`{ #format }

:   **Optional**-*List[DATA_FORMAT]*- supported format/encoding of the data produced or consumed by the data resource as a MIME type (IETF RFC 6838 https://www.sitepoint.com/mime-types-complete-list/). More than one can appear here (remote directory with several files).


    === "Example"
        ``` yaml     
        ["application/zip", "image/jpg"]
        ```

`auth_type`{ #auth_type }

:   **Optional**-*List[DATA_AUTH_TYPE]*- supported authentication type


    === "Example"
        ``` yaml     
        ["tls_mutual", "userpass"]
        ```

`schema`{ #schema }

:   **Optional**-*List[DATA_SCHEMA]*- supported internal message structure, semantics, ontology. It can be any file (doc, rdf, owl, etc.). Asset Administration Shell, IEC 61360 - Common Data Dictionary, …


    === "Example"
        ``` yaml     
        ["jpg"]
        ```

`aux_info`{ #aux_info }

:   **Optional**-*Map[String, String]*- List of key-value pairs (JSON object/YAML dictionary) supported by the data resource. New keys can be added on demand, a list of known keys is available.


    === "Example"
        ``` yaml     
        {"PROTOCOL": "http", "MYSQL_DIALECT": "mariadbdialect", "MQTT_PROTOCOL_VERSION": "3.1.1", "KAFKA_BROKER_VERSION": "2.7.0", "S3_REGION": "eu-central-1"}
        ```

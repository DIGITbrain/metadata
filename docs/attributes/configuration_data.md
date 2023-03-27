<style>
  .md-content__button {
    display: none;
  }
</style>
# Configuration Data Fields




The metadata specification for a DIGITbrain Configuration Data
has these fields:

`file_path`{ #file_path }

:   **Optional**-*String*- full path to file including file name


    === "Example"
        ``` yaml     
        "/data/rclone.conf"
        ```

`file_content`{ #file_content }

:   **Optional**-*String*- file content (not binary)


    === "Example"
        ``` yaml     
        "[s3-server]\n    access_key: 123abc"
        ```

`mount_propagation`{ #mount_propagation }

:   **Optional**-*Enum[ "None", "HostToContainer", "Bidirectional" ]*- Enable mountPropagation https://kubernetes.io/docs/concepts/storage/volumes/#mount-propagation . Default: None


    === "Example"
        ``` yaml     
        "Bidirectional"
        ```

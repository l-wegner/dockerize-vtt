# WARNING

Before using this script do a backup of your vtt-data.
This is a work in progress. 
The script works only in the current folder, a timestamped subfolder and the given folders. 

# dockerize-vtt
A script to run FoundryVTT in a docker container.

Grab the download link and execute
```shell
vtt_docker <the-download-link> <the-folder-with-the-vtt-data> <the-backup-folder> [<the-folder-with-the-application-versions>]
```
This will download the application, create a `Dockerfile-<version>` and a docker image `vtt:<version>`. At the end a container named `vtt-<vtt-data-folder-name>-<version>` is created and started.

In the docker container at `/vtt` and in the vtt-data-folder a `VTT_VERSION.txt` file containing the applications version. The version is the vtt-data-folder is verified when creating a container. That version is update after a backup was executed. 

# cf-postgresql-release
A PostgreSQL service for BOSH.

## Usage

* `config/final.yml` configures the blobstore.
* Add all the local blobs by running `bosh add blob <path_to_blob_on_local_system> <package_name>`
* Create a dev release with `bosh create release --force`.

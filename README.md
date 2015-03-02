# cf-postgresql-release
A PostgreSQL service for BOSH.

## Usage

To use the release included:

    $ bosh upload release releases/postgresql-release-1.yml
    $ bosh deployment manifest.yml && bosh deploy

It include 3 errands:
* broker-registrar: To push the broker app and register it with CF.
* broker-deregistrar: De-registers broker and deletes all service instances & bindings.
* smoketest: Checks basic connectivity with the deployed server.

#### Development
* `config/final.yml` configures the blobstore.
* Add all the local blobs by running `bosh add blob <path_to_blob_on_local_system> <package_name>`
* Create a dev release with `bosh create release --force`.

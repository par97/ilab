## Mirror Data Foundation images to enterprise registry

Mirror Data Foundation images to enterprise registry to follow blow steps:

1. Login to registries
2. Start to mirror images
3. Setup the image mirror set

### Login to registries

1. Run the command `docker login registry.redhat.io` to login to Docker registry with your Red Hat® enterprise credentials
2. Run the command `docker login cp.icr.io` to login to IBM Entitled Container Registry by using the IBM entitlement key.
3. Run the command `docker login $LOCAL_ISF_REGISTRY` to login to the Docker registry with your enterprise registry credentials.

### Start to mirror images

1. Create the image set configuration for IBM Fusion Data Foundation
2. Run the command to mirror the images, `oc mirror --config imageset-config-fdf.yaml docker://${TARGET_PATH} --dest-skip-tls --ignore-history`
3. Create the image set configuration for local storage operator and mirror the LSO images with command `oc mirror --config imageset-config-lso.yaml docker://${TARGET_PATH} --dest-skip-tls --ignore-history`
4. Run the command `oc mirror list operators --catalog <enterprise registry host:port>/<target-path>/cpopen/isf-data-foundation-catalog:v4.14` to check whether the image got successfully mirrored to the registry

### Setup the image mirror set

1. Add `ImageDigestMirrorSet` for IBM Fusion Data Foundation
2. Create a CatalogSource named `redhat-operators`
3. Add `ImageTagMirrorSet` for Data Foundation

Now you can go to Service page in IBM Storage Fusion user interface to install Data Foundation service.
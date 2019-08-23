# dcm4chee-arc-cs
DICOM Conformance Statement for dcm4chee-arc-light

# Building

## With docker

Build the docker image:

```
$ docker build -t dcm4chee-arc-cs -f docker/Dockerfile .
```

You can run the docker image and see which different build options are available. As of today, LaTeX is not included on the docker image dependencies, so only HTML/epub/text options can be built.

```
docker run -ti dcm4chee-arc-cs make help
```

Create a build folder in your project for the output of the build:

```
$ mkdir build
```

Then run the image, mounting your build folder inside the container:

```
docker run -ti -v $(pwd)/build:/docs/build dcm4chee-arc-cs make html
```

Then you'll find the docs built on your build folder.

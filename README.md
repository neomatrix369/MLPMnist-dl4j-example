# MLPMnist-dl4j-example: MLPMNist Single Layer [![MLPMNist using DL4J](https://img.shields.io/docker/pulls/neomatrix369/dl4j-mnist-single-layer.svg)](https://hub.docker.com/r/neomatrix369/dl4j-mnist-single-layer)

This repo is a result of the blog post [How to do Deep Learning for Java](https://medium.com/@neomatrix369/how-to-do-deep-learning-for-java-on-the-valohai-platform-eec8ba9f71d8) | [Original post](https://blog.valohai.com/how-to-do-deep-learning-for-java-on-the-valohai-platform). Please refer to the post before considering using this repo to understand better on how to use the different aspects of it.

Original home of the project: https://github.com/neomatrix369/awesome-ai-ml-dl/tree/master/examples/cloud-devops-infra/valohai/MLPMnist

---

Open built-in Terminal from the Android Studio or IntelliJ IDEA. 
If you prefer, use the terminal app on your computer.
In the terminal window, `cd` to the project root directory `MLPMnist-dl4j-example` if not already in.
(_you can use IDE's run-configuration green run button, if you like._)

### Build app

```
mvn package -Djavacpp.platform=linux-x86_64
or
mvn package -Djavacpp.platform=macos-x86_64
or
mvn package -Djavacpp.platform=windows-x86_64
```

### Build app for the docker image


#### Build docker image

```
./buildUberJar.sh
./buildDockerImage.sh
```

#### Push to docker hub

```
./push-docker-image-to-hub.sh
```

### Run app local

```
./runMLPMnist.sh --action train --output-dir /path/to/model/creation/folder
```

followed by

```
./runMLPMnist.sh --action evaluate --output-dir /path/to/model/folder
```

Model file created and seeked for in the respective cases, is called `mlpmnist-single-layer.pb`.

### Run app in docker container

```
./runDockerContainer.sh
```

At the prompt in the container, do the same as mentioned in section [Run app local](#run-app-local).

## Credits

This example has been inspired by the [MLPMNist example](https://github.com/deeplearning4j/dl4j-examples/tree/master/dl4j-examples/src/main/java/org/deeplearning4j/examples/feedforward/mnist) example from DL4J. Credits to the original authors of this example on https://github.com/deeplearning4j/dl4j-examples.

---

Back to [main page (table of contents)](https://github.com/neomatrix369/awesome-ai-ml-dl#awesome-ai-ml-dl-)
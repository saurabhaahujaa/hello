gcc -static -o prog prog.c

buildah build --platform linux/arm64 -t docker.io/sauraahu/hello:v1.0-amd64 .

buildah build --platform linux/arm64 -t docker.io/sauraahu/hello:v1.0-arm64 .

buildah inspect docker.io/sauraahu/hello:v1.0-arm64

buildah manifest create docker.io/sauraahu/hello:v1.0

buildah manifest add docker.io/sauraahu/hello:v1.0 docker.io/sauraahu/hello:v1.0-amd64

buildah manifest add docker.io/sauraahu/hello:v1.0 docker.io/sauraahu/hello:v1.0-arm64

buildah manifest inspect docker.io/sauraahu/hello:v1.0

buildah manifest push --all docker.io/sauraahu/hello:v1.0 "docker://docker.io/sauraahu/hello:v1.0"


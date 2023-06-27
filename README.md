# VoiceDock specs
API specification for VoiceDock.

> This application is under development. Backward compatibility not yet guaranteed

## API
 * [**STT**](docs%2Fvoicedock%2Fextensions%2Fstt%2Fv1%2FREADME.md) ([proto](proto%2Fvoicedock%2Fextensions%2Fstt%2Fv1)) _Speech To Text_
 * [**TTS**](docs%2Fvoicedock%2Fextensions%2Ftts%2Fv1%2FREADME.md) ([proto](docs%2Fvoicedock%2Fextensions%2Ftts%2Fv1)) _Text To Speech_
 * [**AiChat**](docs%2Fvoicedock%2Fextensions%2Faichat%2Fv1%2FREADME.md) ([proto](docs%2Fvoicedock%2Fextensions%2Faichat%2Fv1)) _AI Chat_

## CONTRIBUTING
Create protobuilder docker image:
```bash
cd ci/protobuilder && \
docker build -t protobuilder .
```
Lint proto files:
```bash
docker run --rm -w "/work" -v "$(pwd):/work" bufbuild/buf:latest lint ./proto
```
Generate API documentation:
```bash
docker run --rm -w "/work" -v "$(pwd):/work" protobuilder generate ./proto --template ./proto/buf.gen.yaml
```
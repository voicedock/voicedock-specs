# VoiceDock specs
API specification for VoiceDock.

> A universal API specification for building voice assistants, voice recognition systems, voice synthesis,
> artificial intelligence, and audio processing.

## API
 * [**STT**](docs%2Fvoicedock%2Fcore%2Fstt%2Fv1%2FREADME.md) ([proto](proto%2Fvoicedock%2Fcore%2Fstt%2Fv1)) _Speech To Text_
 * [**TTS**](docs%2Fvoicedock%2Fcore%2Ftts%2Fv1%2FREADME.md) ([proto](docs%2Fvoicedock%2Fcore%2Ftts%2Fv1)) _Text To Speech_
 * [**AiChat**](docs%2Fvoicedock%2Fcore%2Faichat%2Fv1%2FREADME.md) ([proto](docs%2Fvoicedock%2Fcore%2Faichat%2Fv1)) _AI Chat_

## Implementation examples
 * STT - [STT Whisper](https://github.com/voicedock/sttwhisper)
 * TTS - [TTS Piper](https://github.com/voicedock/ttspiper)
 * AiChat - [AI chat llama](https://github.com/voicedock/aichatllama)

## CONTRIBUTING
Lint proto files:
```bash
docker run --rm -w "/work" -v "$(pwd):/work" bufbuild/buf:latest lint ./proto
```
Generate API documentation:
```bash
docker run --rm -w "/work" -v "$(pwd):/work" ghcr.io/voicedock/protobuilder:1.0.0 generate ./proto --template ./proto/buf.gen.yaml
```
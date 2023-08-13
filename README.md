# VoiceDock specs
API specification for VoiceDock.

> A universal API specification for building voice assistants, voice recognition systems, voice synthesis,
> artificial intelligence, and audio processing.

## API
 * [**STT**](docs%2Fvoicedock%2Fcore%2Fstt%2Fv1%2FREADME.md) ([proto](proto%2Fvoicedock%2Fcore%2Fstt%2Fv1)) _Speech To Text service_
 * [**TTS**](docs%2Fvoicedock%2Fcore%2Ftts%2Fv1%2FREADME.md) ([proto](proto%2Fvoicedock%2Fcore%2Ftts%2Fv1)) _Text To Speech service_
 * [**AI Chat**](docs%2Fvoicedock%2Fcore%2Faichat%2Fv1%2FREADME.md) ([proto](proto%2Fvoicedock%2Fcore%2Faichat%2Fv1)) _AI text chat service_
 * [**SP**](docs%2Fvoicedock%2Fcore%2Fsp%2Fv1%2FREADME.md) ([proto](proto%2Fvoicedock%2Fcore%2Fsp%2Fv1)) _Sound processing service_

## Implementation examples
 * STT - [STT Whisper](https://github.com/voicedock/sttwhisper)
 * TTS - [TTS Piper](https://github.com/voicedock/ttspiper)
 * AiChat - [AI chat llama](https://github.com/voicedock/aichatllama)
 * SP - Coming soon...

## CONTRIBUTING
Lint proto files:
```bash
docker run --rm -w "/work" -v "$(pwd):/work" bufbuild/buf:latest lint ./proto
```
Generate API documentation:
```bash
docker run --rm -w "/work" -v "$(pwd):/work" ghcr.io/voicedock/protobuilder:1.0.0 generate ./proto --template ./proto/buf.gen.yaml
```
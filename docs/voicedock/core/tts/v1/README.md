# Protocol Documentation
<a name="top"></a>

## Table of Contents

- [voicedock/core/tts/v1/tts.proto](#voicedock_core_tts_v1_tts-proto)
    - [Voice](#voicedock-core-tts-v1-Voice)
  
- [voicedock/core/tts/v1/tts_api.proto](#voicedock_core_tts_v1_tts_api-proto)
    - [DownloadVoiceRequest](#voicedock-core-tts-v1-DownloadVoiceRequest)
    - [DownloadVoiceResponse](#voicedock-core-tts-v1-DownloadVoiceResponse)
    - [GetVoicesRequest](#voicedock-core-tts-v1-GetVoicesRequest)
    - [GetVoicesResponse](#voicedock-core-tts-v1-GetVoicesResponse)
    - [TextToSpeechRequest](#voicedock-core-tts-v1-TextToSpeechRequest)
    - [TextToSpeechResponse](#voicedock-core-tts-v1-TextToSpeechResponse)
  
    - [TtsAPI](#voicedock-core-tts-v1-TtsAPI)
  
- [Scalar Value Types](#scalar-value-types)



<a name="voicedock_core_tts_v1_tts-proto"></a>
<p align="right"><a href="#top">Top</a></p>

## voicedock/core/tts/v1/tts.proto



<a name="voicedock-core-tts-v1-Voice"></a>

### Voice
Voice info.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| lang | [string](#string) |  | Language code |
| speaker | [string](#string) |  | Speaker name |
| downloaded | [bool](#bool) |  | Is downloaded |
| downloadable | [bool](#bool) |  | Can be downloaded |
| license | [string](#string) |  | License text to accept |





 

 

 

 



<a name="voicedock_core_tts_v1_tts_api-proto"></a>
<p align="right"><a href="#top">Top</a></p>

## voicedock/core/tts/v1/tts_api.proto



<a name="voicedock-core-tts-v1-DownloadVoiceRequest"></a>

### DownloadVoiceRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| lang | [string](#string) |  | Language. |
| speaker | [string](#string) |  | Speaker. |






<a name="voicedock-core-tts-v1-DownloadVoiceResponse"></a>

### DownloadVoiceResponse







<a name="voicedock-core-tts-v1-GetVoicesRequest"></a>

### GetVoicesRequest







<a name="voicedock-core-tts-v1-GetVoicesResponse"></a>

### GetVoicesResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| voices | [Voice](#voicedock-core-tts-v1-Voice) | repeated |  |






<a name="voicedock-core-tts-v1-TextToSpeechRequest"></a>

### TextToSpeechRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| text | [string](#string) |  | Text phrase to be voiced |
| lang | [string](#string) |  | Language. |
| speaker | [string](#string) |  | Speaker. |






<a name="voicedock-core-tts-v1-TextToSpeechResponse"></a>

### TextToSpeechResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| audio | [voicedock.core.common.v1.AudioContainer](#voicedock-core-common-v1-AudioContainer) |  | Audio stream |





 

 

 


<a name="voicedock-core-tts-v1-TtsAPI"></a>

### TtsAPI
Text-to-speech service.

| Method Name | Request Type | Response Type | Description |
| ----------- | ------------ | ------------- | ------------|
| TextToSpeech | [TextToSpeechRequest](#voicedock-core-tts-v1-TextToSpeechRequest) | [TextToSpeechResponse](#voicedock-core-tts-v1-TextToSpeechResponse) stream | Converts text to speech. |
| GetVoices | [GetVoicesRequest](#voicedock-core-tts-v1-GetVoicesRequest) | [GetVoicesResponse](#voicedock-core-tts-v1-GetVoicesResponse) | Returns available voices. |
| DownloadVoice | [DownloadVoiceRequest](#voicedock-core-tts-v1-DownloadVoiceRequest) | [DownloadVoiceResponse](#voicedock-core-tts-v1-DownloadVoiceResponse) | Downloads selected voice. |

 



## Scalar Value Types

| .proto Type | Notes | C++ | Java | Python | Go | C# | PHP | Ruby |
| ----------- | ----- | --- | ---- | ------ | -- | -- | --- | ---- |
| <a name="double" /> double |  | double | double | float | float64 | double | float | Float |
| <a name="float" /> float |  | float | float | float | float32 | float | float | Float |
| <a name="int32" /> int32 | Uses variable-length encoding. Inefficient for encoding negative numbers – if your field is likely to have negative values, use sint32 instead. | int32 | int | int | int32 | int | integer | Bignum or Fixnum (as required) |
| <a name="int64" /> int64 | Uses variable-length encoding. Inefficient for encoding negative numbers – if your field is likely to have negative values, use sint64 instead. | int64 | long | int/long | int64 | long | integer/string | Bignum |
| <a name="uint32" /> uint32 | Uses variable-length encoding. | uint32 | int | int/long | uint32 | uint | integer | Bignum or Fixnum (as required) |
| <a name="uint64" /> uint64 | Uses variable-length encoding. | uint64 | long | int/long | uint64 | ulong | integer/string | Bignum or Fixnum (as required) |
| <a name="sint32" /> sint32 | Uses variable-length encoding. Signed int value. These more efficiently encode negative numbers than regular int32s. | int32 | int | int | int32 | int | integer | Bignum or Fixnum (as required) |
| <a name="sint64" /> sint64 | Uses variable-length encoding. Signed int value. These more efficiently encode negative numbers than regular int64s. | int64 | long | int/long | int64 | long | integer/string | Bignum |
| <a name="fixed32" /> fixed32 | Always four bytes. More efficient than uint32 if values are often greater than 2^28. | uint32 | int | int | uint32 | uint | integer | Bignum or Fixnum (as required) |
| <a name="fixed64" /> fixed64 | Always eight bytes. More efficient than uint64 if values are often greater than 2^56. | uint64 | long | int/long | uint64 | ulong | integer/string | Bignum |
| <a name="sfixed32" /> sfixed32 | Always four bytes. | int32 | int | int | int32 | int | integer | Bignum or Fixnum (as required) |
| <a name="sfixed64" /> sfixed64 | Always eight bytes. | int64 | long | int/long | int64 | long | integer/string | Bignum |
| <a name="bool" /> bool |  | bool | boolean | boolean | bool | bool | boolean | TrueClass/FalseClass |
| <a name="string" /> string | A string must always contain UTF-8 encoded or 7-bit ASCII text. | string | String | str/unicode | string | string | string | String (UTF-8) |
| <a name="bytes" /> bytes | May contain any arbitrary sequence of bytes. | string | ByteString | str | []byte | ByteString | string | String (ASCII-8BIT) |


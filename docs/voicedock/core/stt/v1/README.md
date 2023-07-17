# Protocol Documentation
<a name="top"></a>

## Table of Contents

- [voicedock/core/stt/v1/stt.proto](#voicedock_core_stt_v1_stt-proto)
    - [LanguagePack](#voicedock-core-stt-v1-LanguagePack)
  
- [voicedock/core/stt/v1/stt_api.proto](#voicedock_core_stt_v1_stt_api-proto)
    - [DownloadLanguagePackRequest](#voicedock-core-stt-v1-DownloadLanguagePackRequest)
    - [DownloadLanguagePackResponse](#voicedock-core-stt-v1-DownloadLanguagePackResponse)
    - [GetLanguagePacksRequest](#voicedock-core-stt-v1-GetLanguagePacksRequest)
    - [GetLanguagePacksResponse](#voicedock-core-stt-v1-GetLanguagePacksResponse)
    - [SpeechToTextRequest](#voicedock-core-stt-v1-SpeechToTextRequest)
    - [SpeechToTextResponse](#voicedock-core-stt-v1-SpeechToTextResponse)
  
    - [SttAPI](#voicedock-core-stt-v1-SttAPI)
  
- [Scalar Value Types](#scalar-value-types)



<a name="voicedock_core_stt_v1_stt-proto"></a>
<p align="right"><a href="#top">Top</a></p>

## voicedock/core/stt/v1/stt.proto



<a name="voicedock-core-stt-v1-LanguagePack"></a>

### LanguagePack
Language pack info.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | Language pack name |
| languages | [string](#string) | repeated | Support language codes |
| downloaded | [bool](#bool) |  | Is downloaded |
| downloadable | [bool](#bool) |  | Can be downloaded |
| license | [string](#string) |  | License text to accept |





 

 

 

 



<a name="voicedock_core_stt_v1_stt_api-proto"></a>
<p align="right"><a href="#top">Top</a></p>

## voicedock/core/stt/v1/stt_api.proto



<a name="voicedock-core-stt-v1-DownloadLanguagePackRequest"></a>

### DownloadLanguagePackRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | Language pack name. |






<a name="voicedock-core-stt-v1-DownloadLanguagePackResponse"></a>

### DownloadLanguagePackResponse







<a name="voicedock-core-stt-v1-GetLanguagePacksRequest"></a>

### GetLanguagePacksRequest







<a name="voicedock-core-stt-v1-GetLanguagePacksResponse"></a>

### GetLanguagePacksResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| languages | [LanguagePack](#voicedock-core-stt-v1-LanguagePack) | repeated |  |






<a name="voicedock-core-stt-v1-SpeechToTextRequest"></a>

### SpeechToTextRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| audio | [voicedock.core.common.v1.AudioContainer](#voicedock-core-common-v1-AudioContainer) |  | Audio stream |
| lang | [string](#string) |  | Audio language |






<a name="voicedock-core-stt-v1-SpeechToTextResponse"></a>

### SpeechToTextResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| token_text | [string](#string) |  | Text token |
| token_probability | [float](#float) |  | Text recognition probability |





 

 

 


<a name="voicedock-core-stt-v1-SttAPI"></a>

### SttAPI
Speech-to-text service.

| Method Name | Request Type | Response Type | Description |
| ----------- | ------------ | ------------- | ------------|
| SpeechToText | [SpeechToTextRequest](#voicedock-core-stt-v1-SpeechToTextRequest) stream | [SpeechToTextResponse](#voicedock-core-stt-v1-SpeechToTextResponse) stream | Converts speech to text. |
| GetLanguagePacks | [GetLanguagePacksRequest](#voicedock-core-stt-v1-GetLanguagePacksRequest) | [GetLanguagePacksResponse](#voicedock-core-stt-v1-GetLanguagePacksResponse) | Returns available language packs. |
| DownloadLanguagePack | [DownloadLanguagePackRequest](#voicedock-core-stt-v1-DownloadLanguagePackRequest) | [DownloadLanguagePackResponse](#voicedock-core-stt-v1-DownloadLanguagePackResponse) | Downloads selected language pack. |

 



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


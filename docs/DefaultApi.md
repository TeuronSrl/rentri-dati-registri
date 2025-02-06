# rentri_dati_registri.DefaultApi

All URIs are relative to *https://demoapi.rentri.gov.it/dati-registri/v1.0*

Method | HTTP request | Description
------------- | ------------- | -------------
[**identificativo_registro_last_transazione_id_get**](DefaultApi.md#identificativo_registro_last_transazione_id_get) | **GET** /{identificativo_registro}/last-transazione-id | Riferimento ultima transazione
[**status_get**](DefaultApi.md#status_get) | **GET** /status | Stato API
[**transazione_id_result_get**](DefaultApi.md#transazione_id_result_get) | **GET** /{transazione_id}/result | Esito transazione
[**transazione_id_status_get**](DefaultApi.md#transazione_id_status_get) | **GET** /{transazione_id}/status | Stato transazione


# **identificativo_registro_last_transazione_id_get**
> TransazioneModel identificativo_registro_last_transazione_id_get(identificativo_registro)

Riferimento ultima transazione

Ritorna il riferimento generato dal sistema relativo all'ultima trasmissione delle registrazioni per il Registro specificato.<hr/><i>Servizio richiamabile in modalità <b>STUB</b> (le richieste restituiranno sempre una risposta vuota) anche in ambiente di produzione.</i><hr/>

### Example

* Bearer (JWT) Authentication (Bearer):
```python
import time
import os
import rentri_dati_registri
from rentri_dati_registri.models.transazione_model import TransazioneModel
from rentri_dati_registri.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://demoapi.rentri.gov.it/dati-registri/v1.0
# See configuration.py for a list of all supported configuration parameters.
configuration = rentri_dati_registri.Configuration(
    host = "https://demoapi.rentri.gov.it/dati-registri/v1.0"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (JWT): Bearer
configuration = rentri_dati_registri.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with rentri_dati_registri.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = rentri_dati_registri.DefaultApi(api_client)
    identificativo_registro = 'identificativo_registro_example' # str | Identificativo del Registro.

    try:
        # Riferimento ultima transazione
        api_response = api_instance.identificativo_registro_last_transazione_id_get(identificativo_registro)
        print("The response of DefaultApi->identificativo_registro_last_transazione_id_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DefaultApi->identificativo_registro_last_transazione_id_get: %s\n" % e)
```



### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **identificativo_registro** | **str**| Identificativo del Registro. | 

### Return type

[**TransazioneModel**](TransazioneModel.md)

### Authorization

[Bearer](../README.md#Bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Riferimento relativo all&#39;ultima transazione. |  -  |
**403** | Operazione non consentita sul Registro. |  -  |
**500** | Errore non gestito (contattare l&#39;assistenza). |  -  |
**429** | Troppe richieste. Questa risposta viene restituita quando vengono rilevate più di 100 richieste in 5s, in caso occorre attendere 10s per effettuare una nuova richiesta. |  * Retry-After - Indica quanto tempo il fruitore deve attendere prima di effettuare una nuova richiesta. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **status_get**
> status_get()

Stato API

Verifica dello stato dell'API.<hr/><i>Servizio richiamabile in modalità <b>STUB</b> (le richieste restituiranno sempre un codice di stato 422) anche in ambiente di produzione.</i><hr/>

### Example

* Bearer (JWT) Authentication (Bearer):
```python
import time
import os
import rentri_dati_registri
from rentri_dati_registri.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://demoapi.rentri.gov.it/dati-registri/v1.0
# See configuration.py for a list of all supported configuration parameters.
configuration = rentri_dati_registri.Configuration(
    host = "https://demoapi.rentri.gov.it/dati-registri/v1.0"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (JWT): Bearer
configuration = rentri_dati_registri.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with rentri_dati_registri.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = rentri_dati_registri.DefaultApi(api_client)

    try:
        # Stato API
        api_instance.status_get()
    except Exception as e:
        print("Exception when calling DefaultApi->status_get: %s\n" % e)
```



### Parameters
This endpoint does not need any parameter.

### Return type

void (empty response body)

### Authorization

[Bearer](../README.md#Bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |
**500** | Internal Server Error |  -  |
**429** | Troppe richieste. Questa risposta viene restituita quando vengono rilevate più di 100 richieste in 5s, in caso occorre attendere 10s per effettuare una nuova richiesta. |  * Retry-After - Indica quanto tempo il fruitore deve attendere prima di effettuare una nuova richiesta. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **transazione_id_result_get**
> TransazioneIdResultGet200Response transazione_id_result_get(transazione_id)

Esito transazione

Ottiene l'esito dell'elaborazione di una richiesta di trasmissione registrazioni.<hr/><i>Servizio richiamabile in modalità <b>STUB</b> (le richieste restituiranno sempre una risposta vuota) anche in ambiente di produzione.</i><hr/>

### Example

* Bearer (JWT) Authentication (Bearer):
```python
import time
import os
import rentri_dati_registri
from rentri_dati_registri.models.transazione_id_result_get200_response import TransazioneIdResultGet200Response
from rentri_dati_registri.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://demoapi.rentri.gov.it/dati-registri/v1.0
# See configuration.py for a list of all supported configuration parameters.
configuration = rentri_dati_registri.Configuration(
    host = "https://demoapi.rentri.gov.it/dati-registri/v1.0"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (JWT): Bearer
configuration = rentri_dati_registri.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with rentri_dati_registri.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = rentri_dati_registri.DefaultApi(api_client)
    transazione_id = 'transazione_id_example' # str | Id della richiesta

    try:
        # Esito transazione
        api_response = api_instance.transazione_id_result_get(transazione_id)
        print("The response of DefaultApi->transazione_id_result_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DefaultApi->transazione_id_result_get: %s\n" % e)
```



### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **transazione_id** | **str**| Id della richiesta | 

### Return type

[**TransazioneIdResultGet200Response**](TransazioneIdResultGet200Response.md)

### Authorization

[Bearer](../README.md#Bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Esito dell&#39;elaborazione con eventuali errori. |  -  |
**400** | Richiesta non ancora elaborata. |  -  |
**403** | Operazione non consentita. |  -  |
**404** | Richiesta non trovata. |  -  |
**500** | Errore non gestito (contattare l&#39;assistenza). |  -  |
**429** | Troppe richieste. Questa risposta viene restituita quando vengono rilevate più di 100 richieste in 5s, in caso occorre attendere 10s per effettuare una nuova richiesta. |  * Retry-After - Indica quanto tempo il fruitore deve attendere prima di effettuare una nuova richiesta. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **transazione_id_status_get**
> transazione_id_status_get(transazione_id)

Stato transazione

Ottiene lo stato di elaborazione di una richiesta di trasmissione registrazioni.<hr/><i>Servizio richiamabile in modalità <b>STUB</b> (le richieste restituiranno sempre una risposta vuota) anche in ambiente di produzione.</i><hr/>

### Example

* Bearer (JWT) Authentication (Bearer):
```python
import time
import os
import rentri_dati_registri
from rentri_dati_registri.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://demoapi.rentri.gov.it/dati-registri/v1.0
# See configuration.py for a list of all supported configuration parameters.
configuration = rentri_dati_registri.Configuration(
    host = "https://demoapi.rentri.gov.it/dati-registri/v1.0"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (JWT): Bearer
configuration = rentri_dati_registri.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with rentri_dati_registri.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = rentri_dati_registri.DefaultApi(api_client)
    transazione_id = 'transazione_id_example' # str | Id della richiesta.

    try:
        # Stato transazione
        api_instance.transazione_id_status_get(transazione_id)
    except Exception as e:
        print("Exception when calling DefaultApi->transazione_id_status_get: %s\n" % e)
```



### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **transazione_id** | **str**| Id della richiesta. | 

### Return type

void (empty response body)

### Authorization

[Bearer](../README.md#Bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Richiesta non ancora elaborata. |  -  |
**303** | La richiesta è stata elaborata e l&#39;URL per il recupero dell&#39;esito si trova nell&#39;header Location. |  * Location - URL per verificare lo stato dell&#39;elaborazione. Restituito solo se non viene specificata una URL di callback nell&#39;header X-ReplyTo. <br>  |
**400** | Bad Request |  -  |
**403** | Operazione non consentita. |  -  |
**404** | Richiesta non trovata. |  -  |
**500** | Errore non gestito (contattare l&#39;assistenza). |  -  |
**429** | Troppe richieste. Questa risposta viene restituita quando vengono rilevate più di 100 richieste in 5s, in caso occorre attendere 10s per effettuare una nuova richiesta. |  * Retry-After - Indica quanto tempo il fruitore deve attendere prima di effettuare una nuova richiesta. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


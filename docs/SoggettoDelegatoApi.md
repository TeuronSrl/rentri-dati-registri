# rentri_dati_registri.SoggettoDelegatoApi

All URIs are relative to *https://demoapi.rentri.gov.it/dati-registri/v1.0*

Method | HTTP request | Description
------------- | ------------- | -------------
[**soggetto_delegato_identificativo_registro_movimenti_count_get**](SoggettoDelegatoApi.md#soggetto_delegato_identificativo_registro_movimenti_count_get) | **GET** /soggetto-delegato/{identificativo_registro}/movimenti/count | Conteggio registrazioni
[**soggetto_delegato_identificativo_registro_movimenti_get**](SoggettoDelegatoApi.md#soggetto_delegato_identificativo_registro_movimenti_get) | **GET** /soggetto-delegato/{identificativo_registro}/movimenti | Elenco registrazioni
[**soggetto_delegato_identificativo_registro_movimenti_post**](SoggettoDelegatoApi.md#soggetto_delegato_identificativo_registro_movimenti_post) | **POST** /soggetto-delegato/{identificativo_registro}/movimenti | 🔁[ASYNC] Trasmissione delle registrazioni
[**soggetto_delegato_identificativo_registro_movimento_anno_progressivo_get**](SoggettoDelegatoApi.md#soggetto_delegato_identificativo_registro_movimento_anno_progressivo_get) | **GET** /soggetto-delegato/{identificativo_registro}/movimento/{anno}/{progressivo} | Dettaglio registrazione per anno e numero
[**soggetto_delegato_identificativo_registro_movimento_identificativo_movimento_get**](SoggettoDelegatoApi.md#soggetto_delegato_identificativo_registro_movimento_identificativo_movimento_get) | **GET** /soggetto-delegato/{identificativo_registro}/movimento/{identificativo_movimento} | Dettaglio registrazione per identificativo
[**soggetto_delegato_identificativo_registro_valida_post**](SoggettoDelegatoApi.md#soggetto_delegato_identificativo_registro_valida_post) | **POST** /soggetto-delegato/{identificativo_registro}/valida | 🔁[ASYNC] Verifica il registro informatico locale
[**soggetto_delegato_num_iscr_ass_transazioni_movimenti_num_iscr_sito_get**](SoggettoDelegatoApi.md#soggetto_delegato_num_iscr_ass_transazioni_movimenti_num_iscr_sito_get) | **GET** /soggetto-delegato/{num_iscr_ass}/transazioni/movimenti/{num_iscr_sito} | Elenco transazioni
[**soggetto_delegato_num_iscr_ass_transazioni_movimenti_num_iscr_sito_identificativo_transazione_get**](SoggettoDelegatoApi.md#soggetto_delegato_num_iscr_ass_transazioni_movimenti_num_iscr_sito_identificativo_transazione_get) | **GET** /soggetto-delegato/{num_iscr_ass}/transazioni/movimenti/{num_iscr_sito}/{identificativo_transazione} | Dettaglio transazione
[**soggetto_delegato_num_iscr_ass_transazioni_movimenti_num_iscr_sito_identificativo_transazione_request_get**](SoggettoDelegatoApi.md#soggetto_delegato_num_iscr_ass_transazioni_movimenti_num_iscr_sito_identificativo_transazione_request_get) | **GET** /soggetto-delegato/{num_iscr_ass}/transazioni/movimenti/{num_iscr_sito}/{identificativo_transazione}/request | Request transazione


# **soggetto_delegato_identificativo_registro_movimenti_count_get**
> int soggetto_delegato_identificativo_registro_movimenti_count_get(identificativo_registro, identificativi_movimento=identificativi_movimento, anno=anno, progressivo=progressivo, alla_data=alla_data, anno_data_registrazione=anno_data_registrazione, data_registrazione_da=data_registrazione_da, data_registrazione_a=data_registrazione_a, causali_operazione=causali_operazione, codice_eer=codice_eer, caratteristiche_pericolo=caratteristiche_pericolo, stato_fisico=stato_fisico, unita_misura=unita_misura, stato_esito_conferimento=stato_esito_conferimento, annullato=annullato, rettificato=rettificato, incompleto=incompleto)

Conteggio registrazioni

Ottiene il conteggio delle registrazioni relative associate ad un Registro, filtrate in base ai criteri specificati.  Specificando un valore per il filtro \"allaData\", si ottiene il conteggio delle registrazioni trasmesse fino a quella data.<hr/><i>Servizio richiamabile in modalità <b>STUB</b> (le richieste restituiranno sempre una risposta vuota) anche in ambiente di produzione.</i><hr/>

### Example

* Bearer (JWT) Authentication (Bearer):
```python
import time
import os
import rentri_dati_registri
from rentri_dati_registri.models.caratteristiche_pericolo import CaratteristichePericolo
from rentri_dati_registri.models.causali_operazione import CausaliOperazione
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
    api_instance = rentri_dati_registri.SoggettoDelegatoApi(api_client)
    identificativo_registro = 'identificativo_registro_example' # str | Identificativo del Registro.
    identificativi_movimento = ['identificativi_movimento_example'] # List[str] |  (optional)
    anno = 56 # int |  (optional)
    progressivo = 56 # int |  (optional)
    alla_data = '2013-10-20T19:20:30+01:00' # datetime | Data di validità (formato ISO 8601 UTC) (optional)
    anno_data_registrazione = 56 # int |  (optional)
    data_registrazione_da = '2013-10-20T19:20:30+01:00' # datetime | Dalla data (formato ISO 8601 UTC) (optional)
    data_registrazione_a = '2013-10-20T19:20:30+01:00' # datetime | Alla data (formato ISO 8601 UTC) (optional)
    causali_operazione = [rentri_dati_registri.CausaliOperazione()] # List[CausaliOperazione] |  (optional)
    codice_eer = 'codice_eer_example' # str |  (optional)
    caratteristiche_pericolo = [rentri_dati_registri.CaratteristichePericolo()] # List[CaratteristichePericolo] |  (optional)
    stato_fisico = rentri_dati_registri.StatiFisici() # StatiFisici |  (optional)
    unita_misura = rentri_dati_registri.UnitaMisura() # UnitaMisura |  (optional)
    stato_esito_conferimento = rentri_dati_registri.StatiEsitoConferimento() # StatiEsitoConferimento |  (optional)
    annullato = True # bool |  (optional)
    rettificato = True # bool |  (optional)
    incompleto = True # bool |  (optional)

    try:
        # Conteggio registrazioni
        api_response = api_instance.soggetto_delegato_identificativo_registro_movimenti_count_get(identificativo_registro, identificativi_movimento=identificativi_movimento, anno=anno, progressivo=progressivo, alla_data=alla_data, anno_data_registrazione=anno_data_registrazione, data_registrazione_da=data_registrazione_da, data_registrazione_a=data_registrazione_a, causali_operazione=causali_operazione, codice_eer=codice_eer, caratteristiche_pericolo=caratteristiche_pericolo, stato_fisico=stato_fisico, unita_misura=unita_misura, stato_esito_conferimento=stato_esito_conferimento, annullato=annullato, rettificato=rettificato, incompleto=incompleto)
        print("The response of SoggettoDelegatoApi->soggetto_delegato_identificativo_registro_movimenti_count_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SoggettoDelegatoApi->soggetto_delegato_identificativo_registro_movimenti_count_get: %s\n" % e)
```



### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **identificativo_registro** | **str**| Identificativo del Registro. | 
 **identificativi_movimento** | [**List[str]**](str.md)|  | [optional] 
 **anno** | **int**|  | [optional] 
 **progressivo** | **int**|  | [optional] 
 **alla_data** | **datetime**| Data di validità (formato ISO 8601 UTC) | [optional] 
 **anno_data_registrazione** | **int**|  | [optional] 
 **data_registrazione_da** | **datetime**| Dalla data (formato ISO 8601 UTC) | [optional] 
 **data_registrazione_a** | **datetime**| Alla data (formato ISO 8601 UTC) | [optional] 
 **causali_operazione** | [**List[CausaliOperazione]**](CausaliOperazione.md)|  | [optional] 
 **codice_eer** | **str**|  | [optional] 
 **caratteristiche_pericolo** | [**List[CaratteristichePericolo]**](CaratteristichePericolo.md)|  | [optional] 
 **stato_fisico** | [**StatiFisici**](.md)|  | [optional] 
 **unita_misura** | [**UnitaMisura**](.md)|  | [optional] 
 **stato_esito_conferimento** | [**StatiEsitoConferimento**](.md)|  | [optional] 
 **annullato** | **bool**|  | [optional] 
 **rettificato** | **bool**|  | [optional] 
 **incompleto** | **bool**|  | [optional] 

### Return type

**int**

### Authorization

[Bearer](../README.md#Bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Conteggio delle registrazioni correnti al momento indicato corrispondenti ai criteri di ricerca specificati. |  -  |
**403** | Operazione non consentita sul Registro. |  -  |
**404** | Registro non trovato. |  -  |
**500** | Errore non gestito (contattare l&#39;assistenza). |  -  |
**429** | Troppe richieste. Questa risposta viene restituita quando vengono rilevate più di 100 richieste in 5s, in caso occorre attendere 10s per effettuare una nuova richiesta. |  * Retry-After - Indica quanto tempo il fruitore deve attendere prima di effettuare una nuova richiesta. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **soggetto_delegato_identificativo_registro_movimenti_get**
> List[DatiMovimentoModel] soggetto_delegato_identificativo_registro_movimenti_get(identificativo_registro, identificativi_movimento=identificativi_movimento, anno=anno, progressivo=progressivo, alla_data=alla_data, anno_data_registrazione=anno_data_registrazione, data_registrazione_da=data_registrazione_da, data_registrazione_a=data_registrazione_a, causali_operazione=causali_operazione, codice_eer=codice_eer, caratteristiche_pericolo=caratteristiche_pericolo, stato_fisico=stato_fisico, unita_misura=unita_misura, stato_esito_conferimento=stato_esito_conferimento, annullato=annullato, rettificato=rettificato, incompleto=incompleto, paging_page=paging_page, paging_page_size=paging_page_size)

Elenco registrazioni

Ottiene l'elenco delle registrazioni relative ad un Registro, filtrate in base ai criteri specificati.  Specificando un valore per il filtro \"allaData\", si ottiene l'elenco delle registrazioni trasmesse fino a quella data.<hr/><i>Servizio richiamabile in modalità <b>STUB</b> (le richieste restituiranno sempre una risposta vuota) anche in ambiente di produzione.</i><hr/>

### Example

* Bearer (JWT) Authentication (Bearer):
```python
import time
import os
import rentri_dati_registri
from rentri_dati_registri.models.caratteristiche_pericolo import CaratteristichePericolo
from rentri_dati_registri.models.causali_operazione import CausaliOperazione
from rentri_dati_registri.models.dati_movimento_model import DatiMovimentoModel
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
    api_instance = rentri_dati_registri.SoggettoDelegatoApi(api_client)
    identificativo_registro = 'identificativo_registro_example' # str | Identificativo del Registro.
    identificativi_movimento = ['identificativi_movimento_example'] # List[str] |  (optional)
    anno = 56 # int |  (optional)
    progressivo = 56 # int |  (optional)
    alla_data = '2013-10-20T19:20:30+01:00' # datetime | Data di validità (formato ISO 8601 UTC) (optional)
    anno_data_registrazione = 56 # int |  (optional)
    data_registrazione_da = '2013-10-20T19:20:30+01:00' # datetime | Dalla data (formato ISO 8601 UTC) (optional)
    data_registrazione_a = '2013-10-20T19:20:30+01:00' # datetime | Alla data (formato ISO 8601 UTC) (optional)
    causali_operazione = [rentri_dati_registri.CausaliOperazione()] # List[CausaliOperazione] |  (optional)
    codice_eer = 'codice_eer_example' # str |  (optional)
    caratteristiche_pericolo = [rentri_dati_registri.CaratteristichePericolo()] # List[CaratteristichePericolo] |  (optional)
    stato_fisico = rentri_dati_registri.StatiFisici() # StatiFisici |  (optional)
    unita_misura = rentri_dati_registri.UnitaMisura() # UnitaMisura |  (optional)
    stato_esito_conferimento = rentri_dati_registri.StatiEsitoConferimento() # StatiEsitoConferimento |  (optional)
    annullato = True # bool |  (optional)
    rettificato = True # bool |  (optional)
    incompleto = True # bool |  (optional)
    paging_page = 1 # int | Valore per l'header Paging-Page. (optional) (default to 1)
    paging_page_size = 100 # int | Valore per l'header Paging-PageSize. (optional) (default to 100)

    try:
        # Elenco registrazioni
        api_response = api_instance.soggetto_delegato_identificativo_registro_movimenti_get(identificativo_registro, identificativi_movimento=identificativi_movimento, anno=anno, progressivo=progressivo, alla_data=alla_data, anno_data_registrazione=anno_data_registrazione, data_registrazione_da=data_registrazione_da, data_registrazione_a=data_registrazione_a, causali_operazione=causali_operazione, codice_eer=codice_eer, caratteristiche_pericolo=caratteristiche_pericolo, stato_fisico=stato_fisico, unita_misura=unita_misura, stato_esito_conferimento=stato_esito_conferimento, annullato=annullato, rettificato=rettificato, incompleto=incompleto, paging_page=paging_page, paging_page_size=paging_page_size)
        print("The response of SoggettoDelegatoApi->soggetto_delegato_identificativo_registro_movimenti_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SoggettoDelegatoApi->soggetto_delegato_identificativo_registro_movimenti_get: %s\n" % e)
```



### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **identificativo_registro** | **str**| Identificativo del Registro. | 
 **identificativi_movimento** | [**List[str]**](str.md)|  | [optional] 
 **anno** | **int**|  | [optional] 
 **progressivo** | **int**|  | [optional] 
 **alla_data** | **datetime**| Data di validità (formato ISO 8601 UTC) | [optional] 
 **anno_data_registrazione** | **int**|  | [optional] 
 **data_registrazione_da** | **datetime**| Dalla data (formato ISO 8601 UTC) | [optional] 
 **data_registrazione_a** | **datetime**| Alla data (formato ISO 8601 UTC) | [optional] 
 **causali_operazione** | [**List[CausaliOperazione]**](CausaliOperazione.md)|  | [optional] 
 **codice_eer** | **str**|  | [optional] 
 **caratteristiche_pericolo** | [**List[CaratteristichePericolo]**](CaratteristichePericolo.md)|  | [optional] 
 **stato_fisico** | [**StatiFisici**](.md)|  | [optional] 
 **unita_misura** | [**UnitaMisura**](.md)|  | [optional] 
 **stato_esito_conferimento** | [**StatiEsitoConferimento**](.md)|  | [optional] 
 **annullato** | **bool**|  | [optional] 
 **rettificato** | **bool**|  | [optional] 
 **incompleto** | **bool**|  | [optional] 
 **paging_page** | **int**| Valore per l&#39;header Paging-Page. | [optional] [default to 1]
 **paging_page_size** | **int**| Valore per l&#39;header Paging-PageSize. | [optional] [default to 100]

### Return type

[**List[DatiMovimentoModel]**](DatiMovimentoModel.md)

### Authorization

[Bearer](../README.md#Bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Elenco delle registrazioni correnti al momento indicato corrispondenti ai criteri di ricerca specificati. |  * Paging-PageCount - Numero totale di pagine. <br>  * Paging-Page - Numero di pagina. <br>  * Paging-PageSize - Dimensione della pagina. <br>  * Paging-TotalRecordCount - Numero totale di record. <br>  |
**403** | Operazione non consentita sul Registro. |  -  |
**404** | Registro non trovato. |  -  |
**500** | Errore non gestito (contattare l&#39;assistenza). |  -  |
**429** | Troppe richieste. Questa risposta viene restituita quando vengono rilevate più di 100 richieste in 5s, in caso occorre attendere 10s per effettuare una nuova richiesta. |  * Retry-After - Indica quanto tempo il fruitore deve attendere prima di effettuare una nuova richiesta. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **soggetto_delegato_identificativo_registro_movimenti_post**
> TransazioneModel soggetto_delegato_identificativo_registro_movimenti_post(identificativo_registro, operatore_identificativo_registro_movimenti_post_request_inner, x_reply_to=x_reply_to)

🔁[ASYNC] Trasmissione delle registrazioni

Acquisisce la richiesta di trasmissione di registrazioni (nuove, rettifiche, annullamenti) relative ad un Registro.  Con l'identificativo della transazione restituito è possibile consultare lo stato di avanzamento dell'elaborazione e richiederne l'esito.  Ogni richiesta accetta un numero massimo di 1000 registrazioni.<hr/><i>Servizio richiamabile in modalità <b>STUB</b> (le richieste restituiranno sempre un codice di stato 422) anche in ambiente di produzione.</i><hr/><br/>Se viene specificato un URL nell'header X-ReplyTo, al termine dell'elaborazione dei dati, il fruitore riceverà una notifica con l'esito dell'elaborazione all'URL specificato.

### Example

* Bearer (JWT) Authentication (Bearer):
```python
import time
import os
import rentri_dati_registri
from rentri_dati_registri.models.operatore_identificativo_registro_movimenti_post_request_inner import OperatoreIdentificativoRegistroMovimentiPostRequestInner
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
    api_instance = rentri_dati_registri.SoggettoDelegatoApi(api_client)
    identificativo_registro = 'identificativo_registro_example' # str | Identificativo del Registro a cui fanno riferimento le registrazioni.
    operatore_identificativo_registro_movimenti_post_request_inner = [rentri_dati_registri.OperatoreIdentificativoRegistroMovimentiPostRequestInner()] # List[OperatoreIdentificativoRegistroMovimentiPostRequestInner] | Elenco delle registrazioni (nuovi, rettifiche, annullamenti).
    x_reply_to = 'x_reply_to_example' # str | URL a cui il fruitore riceverà la notifica al termine dell'elaborazione (modalità push). (optional)

    try:
        # 🔁[ASYNC] Trasmissione delle registrazioni
        api_response = api_instance.soggetto_delegato_identificativo_registro_movimenti_post(identificativo_registro, operatore_identificativo_registro_movimenti_post_request_inner, x_reply_to=x_reply_to)
        print("The response of SoggettoDelegatoApi->soggetto_delegato_identificativo_registro_movimenti_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SoggettoDelegatoApi->soggetto_delegato_identificativo_registro_movimenti_post: %s\n" % e)
```



### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **identificativo_registro** | **str**| Identificativo del Registro a cui fanno riferimento le registrazioni. | 
 **operatore_identificativo_registro_movimenti_post_request_inner** | [**List[OperatoreIdentificativoRegistroMovimentiPostRequestInner]**](OperatoreIdentificativoRegistroMovimentiPostRequestInner.md)| Elenco delle registrazioni (nuovi, rettifiche, annullamenti). | 
 **x_reply_to** | **str**| URL a cui il fruitore riceverà la notifica al termine dell&#39;elaborazione (modalità push). | [optional] 

### Return type

[**TransazioneModel**](TransazioneModel.md)

### Authorization

[Bearer](../README.md#Bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/problem+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**202** | Richiesta accettata e identificativo della transazione. |  * Location - URL per verificare lo stato dell&#39;elaborazione. Restituito solo se non viene specificata una URL di callback nell&#39;header X-ReplyTo. <br>  |
**400** | Dettaglio degli errori di validazione in caso di modello dati non valido. |  -  |
**403** | Operazione non consentita sul Registro. |  -  |
**404** | Registro non trovato. |  -  |
**500** | Errore non gestito (contattare l&#39;assistenza). |  -  |
**429** | Troppe richieste. Questa risposta viene restituita quando vengono rilevate più di 100 richieste in 5s, in caso occorre attendere 10s per effettuare una nuova richiesta. |  * Retry-After - Indica quanto tempo il fruitore deve attendere prima di effettuare una nuova richiesta. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **soggetto_delegato_identificativo_registro_movimento_anno_progressivo_get**
> MovimentoDettaglioModel soggetto_delegato_identificativo_registro_movimento_anno_progressivo_get(identificativo_registro, anno, progressivo, alla_data=alla_data, variazioni=variazioni)

Dettaglio registrazione per anno e numero

Ottiene il dettaglio di una registrazione specificando anno/numero registrazione.  Specificando un valore per il filtro \"allaData\", si ottiene il dettaglio della registrazione a quella data.<hr/><i>Servizio richiamabile in modalità <b>STUB</b> (le richieste restituiranno sempre una risposta vuota) anche in ambiente di produzione.</i><hr/>

### Example

* Bearer (JWT) Authentication (Bearer):
```python
import time
import os
import rentri_dati_registri
from rentri_dati_registri.models.movimento_dettaglio_model import MovimentoDettaglioModel
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
    api_instance = rentri_dati_registri.SoggettoDelegatoApi(api_client)
    identificativo_registro = 'identificativo_registro_example' # str | Identificativo del Registro.
    anno = 56 # int | Anno della registrazione da recuperare.
    progressivo = 56 # int | Progressivo della registrazione da recuperare.
    alla_data = '2013-10-20T19:20:30+01:00' # datetime | Data di validità dei dati (formato ISO 8601 UTC). (optional)
    variazioni = True # bool | Indica se recuperare anche la storia della registrazione (tutte le sue variazioni). (optional) (default to True)

    try:
        # Dettaglio registrazione per anno e numero
        api_response = api_instance.soggetto_delegato_identificativo_registro_movimento_anno_progressivo_get(identificativo_registro, anno, progressivo, alla_data=alla_data, variazioni=variazioni)
        print("The response of SoggettoDelegatoApi->soggetto_delegato_identificativo_registro_movimento_anno_progressivo_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SoggettoDelegatoApi->soggetto_delegato_identificativo_registro_movimento_anno_progressivo_get: %s\n" % e)
```



### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **identificativo_registro** | **str**| Identificativo del Registro. | 
 **anno** | **int**| Anno della registrazione da recuperare. | 
 **progressivo** | **int**| Progressivo della registrazione da recuperare. | 
 **alla_data** | **datetime**| Data di validità dei dati (formato ISO 8601 UTC). | [optional] 
 **variazioni** | **bool**| Indica se recuperare anche la storia della registrazione (tutte le sue variazioni). | [optional] [default to True]

### Return type

[**MovimentoDettaglioModel**](MovimentoDettaglioModel.md)

### Authorization

[Bearer](../README.md#Bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Dettaglio della registrazione (ed eventuale lista di tutte le sue variazioni) riferita al momento indicato. |  -  |
**403** | Operazione non consentita sul Registro. |  -  |
**404** | Registro o registrazione non trovata. |  -  |
**500** | Errore non gestito (contattare l&#39;assistenza). |  -  |
**429** | Troppe richieste. Questa risposta viene restituita quando vengono rilevate più di 100 richieste in 5s, in caso occorre attendere 10s per effettuare una nuova richiesta. |  * Retry-After - Indica quanto tempo il fruitore deve attendere prima di effettuare una nuova richiesta. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **soggetto_delegato_identificativo_registro_movimento_identificativo_movimento_get**
> MovimentoDettaglioModel soggetto_delegato_identificativo_registro_movimento_identificativo_movimento_get(identificativo_registro, identificativo_movimento, alla_data=alla_data, variazioni=variazioni)

Dettaglio registrazione per identificativo

Ottiene il dettaglio di una registrazione specificando l'identificativo assegnato dal RENTRI al momento della trasmissione.  Specificando un valore per il filtro \"allaData\", si ottiene il dettaglio della registrazione a quella data.<hr/><i>Servizio richiamabile in modalità <b>STUB</b> (le richieste restituiranno sempre una risposta vuota) anche in ambiente di produzione.</i><hr/>

### Example

* Bearer (JWT) Authentication (Bearer):
```python
import time
import os
import rentri_dati_registri
from rentri_dati_registri.models.movimento_dettaglio_model import MovimentoDettaglioModel
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
    api_instance = rentri_dati_registri.SoggettoDelegatoApi(api_client)
    identificativo_registro = 'identificativo_registro_example' # str | Identificativo del Registro.
    identificativo_movimento = 'identificativo_movimento_example' # str | Identificativo della registrazione da recuperare.
    alla_data = '2013-10-20T19:20:30+01:00' # datetime | Data di validità dei dati (formato ISO 8601 UTC). (optional)
    variazioni = True # bool | Indica se recuperare anche la storia della registrazione (tutte le sue variazioni). (optional) (default to True)

    try:
        # Dettaglio registrazione per identificativo
        api_response = api_instance.soggetto_delegato_identificativo_registro_movimento_identificativo_movimento_get(identificativo_registro, identificativo_movimento, alla_data=alla_data, variazioni=variazioni)
        print("The response of SoggettoDelegatoApi->soggetto_delegato_identificativo_registro_movimento_identificativo_movimento_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SoggettoDelegatoApi->soggetto_delegato_identificativo_registro_movimento_identificativo_movimento_get: %s\n" % e)
```



### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **identificativo_registro** | **str**| Identificativo del Registro. | 
 **identificativo_movimento** | **str**| Identificativo della registrazione da recuperare. | 
 **alla_data** | **datetime**| Data di validità dei dati (formato ISO 8601 UTC). | [optional] 
 **variazioni** | **bool**| Indica se recuperare anche la storia della registrazione (tutte le sue variazioni). | [optional] [default to True]

### Return type

[**MovimentoDettaglioModel**](MovimentoDettaglioModel.md)

### Authorization

[Bearer](../README.md#Bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Dettaglio della registrazione (ed eventuale lista di tutte le sue variazioni) riferita al momento indicato. |  -  |
**403** | Operazione non consentita sul Registro. |  -  |
**404** | Registro o registrazione non trovata. |  -  |
**500** | Errore non gestito (contattare l&#39;assistenza). |  -  |
**429** | Troppe richieste. Questa risposta viene restituita quando vengono rilevate più di 100 richieste in 5s, in caso occorre attendere 10s per effettuare una nuova richiesta. |  * Retry-After - Indica quanto tempo il fruitore deve attendere prima di effettuare una nuova richiesta. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **soggetto_delegato_identificativo_registro_valida_post**
> TransazioneModel soggetto_delegato_identificativo_registro_valida_post(identificativo_registro, valida_registro_request, x_reply_to=x_reply_to)

🔁[ASYNC] Verifica il registro informatico locale

Esegue la validazione strutturale del registro cronologico di carico e scarico digitale in formato XML secondo le specifiche tecniche.  Viene eseguita la validazione XSD e tutte le validazioni applicate nella trasmissione delle registrazioni al RENTRI ad  esclusione delle validazioni  in fase di elaborazione elencate in <i>/docs?page=registro-digitale#4-2-validazioni-aggiuntive-in-fase-di-elaborazione</i>.  Inoltre esegue il test di corrispondenza tra la versione locale e i dati già trasmessi al RENTRI.  Acquisisce la richiesta e fornisce in modo asincrono l’esito contenente alcune informazioni estrapolate dal file e la lista dei problemi di validazione divisi in 2 livelli:  <i>Errore</i> (problemi di validazione) e <i>Avvertimento</i> (problemi di non corrispondenza dei dati con quelli già trasmessi al RENTRI).  <hr/><i>Servizio richiamabile in modalità <b>STUB</b> (le richieste restituiranno sempre un codice di stato 422) anche in ambiente di produzione.</i><hr/><br/>Se viene specificato un URL nell'header X-ReplyTo, al termine dell'elaborazione dei dati, il fruitore riceverà una notifica con l'esito dell'elaborazione all'URL specificato.

### Example

* Bearer (JWT) Authentication (Bearer):
```python
import time
import os
import rentri_dati_registri
from rentri_dati_registri.models.transazione_model import TransazioneModel
from rentri_dati_registri.models.valida_registro_request import ValidaRegistroRequest
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
    api_instance = rentri_dati_registri.SoggettoDelegatoApi(api_client)
    identificativo_registro = 'identificativo_registro_example' # str | Identificativo del Registro a cui fanno riferimento le registrazioni.
    valida_registro_request = rentri_dati_registri.ValidaRegistroRequest() # ValidaRegistroRequest | Modello con il file XML da validare. E' permesso anche l'invio di un file XML zippato.
    x_reply_to = 'x_reply_to_example' # str | URL a cui il fruitore riceverà la notifica al termine dell'elaborazione (modalità push). (optional)

    try:
        # 🔁[ASYNC] Verifica il registro informatico locale
        api_response = api_instance.soggetto_delegato_identificativo_registro_valida_post(identificativo_registro, valida_registro_request, x_reply_to=x_reply_to)
        print("The response of SoggettoDelegatoApi->soggetto_delegato_identificativo_registro_valida_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SoggettoDelegatoApi->soggetto_delegato_identificativo_registro_valida_post: %s\n" % e)
```



### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **identificativo_registro** | **str**| Identificativo del Registro a cui fanno riferimento le registrazioni. | 
 **valida_registro_request** | [**ValidaRegistroRequest**](ValidaRegistroRequest.md)| Modello con il file XML da validare. E&#39; permesso anche l&#39;invio di un file XML zippato. | 
 **x_reply_to** | **str**| URL a cui il fruitore riceverà la notifica al termine dell&#39;elaborazione (modalità push). | [optional] 

### Return type

[**TransazioneModel**](TransazioneModel.md)

### Authorization

[Bearer](../README.md#Bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/problem+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**202** | Richiesta accettata e identificativo della transazione. |  * Location - URL per verificare lo stato dell&#39;elaborazione. Restituito solo se non viene specificata una URL di callback nell&#39;header X-ReplyTo. <br>  |
**400** | Dettaglio degli errori di validazione in caso di modello dati non valido. |  -  |
**403** | Operazione non consentita sul Registro. |  -  |
**404** | Registro non trovato. |  -  |
**500** | Errore non gestito (contattare l&#39;assistenza). |  -  |
**429** | Troppe richieste. Questa risposta viene restituita quando vengono rilevate più di 100 richieste in 5s, in caso occorre attendere 10s per effettuare una nuova richiesta. |  * Retry-After - Indica quanto tempo il fruitore deve attendere prima di effettuare una nuova richiesta. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **soggetto_delegato_num_iscr_ass_transazioni_movimenti_num_iscr_sito_get**
> List[InfoTransazioneModel] soggetto_delegato_num_iscr_ass_transazioni_movimenti_num_iscr_sito_get(num_iscr_ass, num_iscr_sito, identificativo_registro=identificativo_registro, anno=anno, identificativo_transazione=identificativo_transazione, sorgente=sorgente, solo_esito_positivo=solo_esito_positivo, paging_page=paging_page, paging_page_size=paging_page_size)

Elenco transazioni

Ottiene l'elenco delle transazioni associate alle richieste di trasmissione delle registrazioni, realtive ad un'unità locale gestita da un soggetto delegato.<hr/><i>Servizio richiamabile in modalità <b>STUB</b> (le richieste restituiranno sempre una risposta vuota) anche in ambiente di produzione.</i><hr/>

### Example

* Bearer (JWT) Authentication (Bearer):
```python
import time
import os
import rentri_dati_registri
from rentri_dati_registri.models.info_transazione_model import InfoTransazioneModel
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
    api_instance = rentri_dati_registri.SoggettoDelegatoApi(api_client)
    num_iscr_ass = 'num_iscr_ass_example' # str | Numero iscrizione soggetto delegato rilasciato all'iscrizione.
    num_iscr_sito = 'num_iscr_sito_example' # str | Numero iscrizione unità locale rilasciato all'iscrizione.
    identificativo_registro = 'identificativo_registro_example' # str | Identificativo del Registro. (optional)
    anno = 56 # int | Anno di riferimento. (optional)
    identificativo_transazione = 'identificativo_transazione_example' # str | Identificativo della transazione. (optional)
    sorgente = rentri_dati_registri.SorgenteTransazione() # SorgenteTransazione | Sorgente della transazione. (optional)
    solo_esito_positivo = True # bool | Indica se recuperare solamente le transazioni che hanno avuto esito positivo. (optional)
    paging_page = 1 # int | Valore per l'header Paging-Page. (optional) (default to 1)
    paging_page_size = 100 # int | Valore per l'header Paging-PageSize. (optional) (default to 100)

    try:
        # Elenco transazioni
        api_response = api_instance.soggetto_delegato_num_iscr_ass_transazioni_movimenti_num_iscr_sito_get(num_iscr_ass, num_iscr_sito, identificativo_registro=identificativo_registro, anno=anno, identificativo_transazione=identificativo_transazione, sorgente=sorgente, solo_esito_positivo=solo_esito_positivo, paging_page=paging_page, paging_page_size=paging_page_size)
        print("The response of SoggettoDelegatoApi->soggetto_delegato_num_iscr_ass_transazioni_movimenti_num_iscr_sito_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SoggettoDelegatoApi->soggetto_delegato_num_iscr_ass_transazioni_movimenti_num_iscr_sito_get: %s\n" % e)
```



### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **num_iscr_ass** | **str**| Numero iscrizione soggetto delegato rilasciato all&#39;iscrizione. | 
 **num_iscr_sito** | **str**| Numero iscrizione unità locale rilasciato all&#39;iscrizione. | 
 **identificativo_registro** | **str**| Identificativo del Registro. | [optional] 
 **anno** | **int**| Anno di riferimento. | [optional] 
 **identificativo_transazione** | **str**| Identificativo della transazione. | [optional] 
 **sorgente** | [**SorgenteTransazione**](.md)| Sorgente della transazione. | [optional] 
 **solo_esito_positivo** | **bool**| Indica se recuperare solamente le transazioni che hanno avuto esito positivo. | [optional] 
 **paging_page** | **int**| Valore per l&#39;header Paging-Page. | [optional] [default to 1]
 **paging_page_size** | **int**| Valore per l&#39;header Paging-PageSize. | [optional] [default to 100]

### Return type

[**List[InfoTransazioneModel]**](InfoTransazioneModel.md)

### Authorization

[Bearer](../README.md#Bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Elenco delle transazioni relative all&#39;unità locale e corrispondenti ai criteri di ricerca specificati. |  * Paging-PageCount - Numero totale di pagine. <br>  * Paging-Page - Numero di pagina. <br>  * Paging-PageSize - Dimensione della pagina. <br>  * Paging-TotalRecordCount - Numero totale di record. <br>  |
**403** | Operazione non consentita. |  -  |
**404** | Operatore o unità locale non trovati. |  -  |
**500** | Errore non gestito (contattare l&#39;assistenza). |  -  |
**429** | Troppe richieste. Questa risposta viene restituita quando vengono rilevate più di 100 richieste in 5s, in caso occorre attendere 10s per effettuare una nuova richiesta. |  * Retry-After - Indica quanto tempo il fruitore deve attendere prima di effettuare una nuova richiesta. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **soggetto_delegato_num_iscr_ass_transazioni_movimenti_num_iscr_sito_identificativo_transazione_get**
> InfoTransazioneDettaglioModel soggetto_delegato_num_iscr_ass_transazioni_movimenti_num_iscr_sito_identificativo_transazione_get(num_iscr_ass, num_iscr_sito, identificativo_transazione)

Dettaglio transazione

Ottiene il dettaglio di una transazione specificando l'identificativo.<hr/><i>Servizio richiamabile in modalità <b>STUB</b> (le richieste restituiranno sempre una risposta vuota) anche in ambiente di produzione.</i><hr/>

### Example

* Bearer (JWT) Authentication (Bearer):
```python
import time
import os
import rentri_dati_registri
from rentri_dati_registri.models.info_transazione_dettaglio_model import InfoTransazioneDettaglioModel
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
    api_instance = rentri_dati_registri.SoggettoDelegatoApi(api_client)
    num_iscr_ass = 'num_iscr_ass_example' # str | Numero iscrizione soggetto delegato rilasciato all'iscrizione.
    num_iscr_sito = 'num_iscr_sito_example' # str | Numero iscrizione unità locale rilasciato all'iscrizione.
    identificativo_transazione = 'identificativo_transazione_example' # str | Identificativo della transazione da recuperare.

    try:
        # Dettaglio transazione
        api_response = api_instance.soggetto_delegato_num_iscr_ass_transazioni_movimenti_num_iscr_sito_identificativo_transazione_get(num_iscr_ass, num_iscr_sito, identificativo_transazione)
        print("The response of SoggettoDelegatoApi->soggetto_delegato_num_iscr_ass_transazioni_movimenti_num_iscr_sito_identificativo_transazione_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SoggettoDelegatoApi->soggetto_delegato_num_iscr_ass_transazioni_movimenti_num_iscr_sito_identificativo_transazione_get: %s\n" % e)
```



### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **num_iscr_ass** | **str**| Numero iscrizione soggetto delegato rilasciato all&#39;iscrizione. | 
 **num_iscr_sito** | **str**| Numero iscrizione unità locale rilasciato all&#39;iscrizione. | 
 **identificativo_transazione** | **str**| Identificativo della transazione da recuperare. | 

### Return type

[**InfoTransazioneDettaglioModel**](InfoTransazioneDettaglioModel.md)

### Authorization

[Bearer](../README.md#Bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Dettaglio della transazione. |  -  |
**403** | Operazione non consentita. |  -  |
**404** | Operatore, unità locale o transazione non trovati. |  -  |
**500** | Errore non gestito (contattare l&#39;assistenza). |  -  |
**429** | Troppe richieste. Questa risposta viene restituita quando vengono rilevate più di 100 richieste in 5s, in caso occorre attendere 10s per effettuare una nuova richiesta. |  * Retry-After - Indica quanto tempo il fruitore deve attendere prima di effettuare una nuova richiesta. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **soggetto_delegato_num_iscr_ass_transazioni_movimenti_num_iscr_sito_identificativo_transazione_request_get**
> TransazioneRequestModel soggetto_delegato_num_iscr_ass_transazioni_movimenti_num_iscr_sito_identificativo_transazione_request_get(num_iscr_ass, num_iscr_sito, identificativo_transazione)

Request transazione

Ottiene la request associata alla transazione specificata.<hr/><i>Servizio richiamabile in modalità <b>STUB</b> (le richieste restituiranno sempre una risposta vuota) anche in ambiente di produzione.</i><hr/>

### Example

* Bearer (JWT) Authentication (Bearer):
```python
import time
import os
import rentri_dati_registri
from rentri_dati_registri.models.transazione_request_model import TransazioneRequestModel
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
    api_instance = rentri_dati_registri.SoggettoDelegatoApi(api_client)
    num_iscr_ass = 'num_iscr_ass_example' # str | Numero iscrizione soggetto delegato rilasciato all'iscrizione.
    num_iscr_sito = 'num_iscr_sito_example' # str | Numero iscrizione unità locale rilasciato all'iscrizione.
    identificativo_transazione = 'identificativo_transazione_example' # str | Identificativo della transazione.

    try:
        # Request transazione
        api_response = api_instance.soggetto_delegato_num_iscr_ass_transazioni_movimenti_num_iscr_sito_identificativo_transazione_request_get(num_iscr_ass, num_iscr_sito, identificativo_transazione)
        print("The response of SoggettoDelegatoApi->soggetto_delegato_num_iscr_ass_transazioni_movimenti_num_iscr_sito_identificativo_transazione_request_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SoggettoDelegatoApi->soggetto_delegato_num_iscr_ass_transazioni_movimenti_num_iscr_sito_identificativo_transazione_request_get: %s\n" % e)
```



### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **num_iscr_ass** | **str**| Numero iscrizione soggetto delegato rilasciato all&#39;iscrizione. | 
 **num_iscr_sito** | **str**| Numero iscrizione unità locale rilasciato all&#39;iscrizione. | 
 **identificativo_transazione** | **str**| Identificativo della transazione. | 

### Return type

[**TransazioneRequestModel**](TransazioneRequestModel.md)

### Authorization

[Bearer](../README.md#Bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Request associata alla transazione. |  -  |
**403** | Operazione non consentita. |  -  |
**404** | Operatore, unità locale o transazione non trovati. |  -  |
**500** | Errore non gestito (contattare l&#39;assistenza). |  -  |
**429** | Troppe richieste. Questa risposta viene restituita quando vengono rilevate più di 100 richieste in 5s, in caso occorre attendere 10s per effettuare una nuova richiesta. |  * Retry-After - Indica quanto tempo il fruitore deve attendere prima di effettuare una nuova richiesta. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


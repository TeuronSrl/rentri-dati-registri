# TransazioneIdResultGet200Response


## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**esito** | [**EsitoValidaRegistroDataModel**](EsitoValidaRegistroDataModel.md) | Dati dell&#39;esito validazione | [optional] 
**transazione_id** | **str** | Identificativo della transazione asincrona | [optional] 
**validazione** | [**List[EsitoMessaggioModel]**](EsitoMessaggioModel.md) | Messaggi di validazione | [optional] 
**errore** | **bool** |  | [optional] [readonly] 
**tempo_elaborazione** | **str** |  | [optional] 

## Example

```python
from rentri_dati_registri.models.transazione_id_result_get200_response import TransazioneIdResultGet200Response

# TODO update the JSON string below
json = "{}"
# create an instance of TransazioneIdResultGet200Response from a JSON string
transazione_id_result_get200_response_instance = TransazioneIdResultGet200Response.from_json(json)
# print the JSON string representation of the object
print TransazioneIdResultGet200Response.to_json()

# convert the object into a dict
transazione_id_result_get200_response_dict = transazione_id_result_get200_response_instance.to_dict()
# create an instance of TransazioneIdResultGet200Response from a dict
transazione_id_result_get200_response_from_dict = TransazioneIdResultGet200Response.from_dict(transazione_id_result_get200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



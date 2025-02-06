# EsitoMovimentiModel

Esito trasmissione della registrazione

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**esito** | [**EsitoMovimentiDataModel**](EsitoMovimentiDataModel.md) | Dati dell&#39;esito della registrazione | [optional] 
**transazione_id** | **str** | Identificativo della transazione asincrona | [optional] 
**validazione** | [**List[EsitoMessaggioModel]**](EsitoMessaggioModel.md) | Messaggi di validazione | [optional] 
**errore** | **bool** |  | [optional] [readonly] 
**tempo_elaborazione** | **str** |  | [optional] 

## Example

```python
from rentri_dati_registri.models.esito_movimenti_model import EsitoMovimentiModel

# TODO update the JSON string below
json = "{}"
# create an instance of EsitoMovimentiModel from a JSON string
esito_movimenti_model_instance = EsitoMovimentiModel.from_json(json)
# print the JSON string representation of the object
print EsitoMovimentiModel.to_json()

# convert the object into a dict
esito_movimenti_model_dict = esito_movimenti_model_instance.to_dict()
# create an instance of EsitoMovimentiModel from a dict
esito_movimenti_model_from_dict = EsitoMovimentiModel.from_dict(esito_movimenti_model_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



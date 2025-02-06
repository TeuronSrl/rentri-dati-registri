# EsitoMovimentiBaseModel


## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**transazione_id** | **str** | Identificativo della transazione asincrona | [optional] 
**validazione** | [**List[EsitoMessaggioModel]**](EsitoMessaggioModel.md) | Messaggi di validazione | [optional] 
**errore** | **bool** |  | [optional] [readonly] 
**tempo_elaborazione** | **str** |  | [optional] 

## Example

```python
from rentri_dati_registri.models.esito_movimenti_base_model import EsitoMovimentiBaseModel

# TODO update the JSON string below
json = "{}"
# create an instance of EsitoMovimentiBaseModel from a JSON string
esito_movimenti_base_model_instance = EsitoMovimentiBaseModel.from_json(json)
# print the JSON string representation of the object
print EsitoMovimentiBaseModel.to_json()

# convert the object into a dict
esito_movimenti_base_model_dict = esito_movimenti_base_model_instance.to_dict()
# create an instance of EsitoMovimentiBaseModel from a dict
esito_movimenti_base_model_from_dict = EsitoMovimentiBaseModel.from_dict(esito_movimenti_base_model_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



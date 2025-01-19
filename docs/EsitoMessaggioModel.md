# EsitoMessaggioModel

Messaggio di validazione

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**indice** | **int** | Indice dell&#39;elemento di input relativo al messaggio di validazione | [optional] 
**campo** | **str** | Campo dell&#39;elemento di input relativo al messaggio di validazione | [optional] 
**tipo** | [**EsitoMessaggioTipo**](EsitoMessaggioTipo.md) | Tipo del messaggio (avvertimento o errore) | [optional] 
**codice_messaggio** | **str** | Codice del messaggio | [optional] 
**parametri** | **List[object]** | Parametri del messaggio | [optional] 

## Example

```python
from rentri_dati_registri.models.esito_messaggio_model import EsitoMessaggioModel

# TODO update the JSON string below
json = "{}"
# create an instance of EsitoMessaggioModel from a JSON string
esito_messaggio_model_instance = EsitoMessaggioModel.from_json(json)
# print the JSON string representation of the object
print(EsitoMessaggioModel.to_json())

# convert the object into a dict
esito_messaggio_model_dict = esito_messaggio_model_instance.to_dict()
# create an instance of EsitoMessaggioModel from a dict
esito_messaggio_model_from_dict = EsitoMessaggioModel.from_dict(esito_messaggio_model_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



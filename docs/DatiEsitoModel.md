# DatiEsitoModel

Esito conferimento

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data_fine_trasporto** | **datetime** | Data di fine trasporto (formato ISO 8601 UTC) | [optional] 
**peso_verificato_destino** | **float** | Peso verificato a destino (parte intera: 10, parte decimale: 4) compreso tra 0.0000 e 9999999999.9999. | [optional] 
**respingimento** | [**DatiRespingimentoModel**](DatiRespingimentoModel.md) | Dati sul respingimento | [optional] 

## Example

```python
from rentri_dati_registri.models.dati_esito_model import DatiEsitoModel

# TODO update the JSON string below
json = "{}"
# create an instance of DatiEsitoModel from a JSON string
dati_esito_model_instance = DatiEsitoModel.from_json(json)
# print the JSON string representation of the object
print DatiEsitoModel.to_json()

# convert the object into a dict
dati_esito_model_dict = dati_esito_model_instance.to_dict()
# create an instance of DatiEsitoModel from a dict
dati_esito_model_from_dict = DatiEsitoModel.from_dict(dati_esito_model_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



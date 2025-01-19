# EsitoMovimentiDataModel


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identificativo_registro** | **str** | Identificativo del registro | [optional] 
**numero_registrazioni** | [**List[IdentificativoMovimentoCompletoModel]**](IdentificativoMovimentoCompletoModel.md) | Elenco degli identificativi delle registrazioni | [optional] 

## Example

```python
from rentri_dati_registri.models.esito_movimenti_data_model import EsitoMovimentiDataModel

# TODO update the JSON string below
json = "{}"
# create an instance of EsitoMovimentiDataModel from a JSON string
esito_movimenti_data_model_instance = EsitoMovimentiDataModel.from_json(json)
# print the JSON string representation of the object
print(EsitoMovimentiDataModel.to_json())

# convert the object into a dict
esito_movimenti_data_model_dict = esito_movimenti_data_model_instance.to_dict()
# create an instance of EsitoMovimentiDataModel from a dict
esito_movimenti_data_model_from_dict = EsitoMovimentiDataModel.from_dict(esito_movimenti_data_model_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



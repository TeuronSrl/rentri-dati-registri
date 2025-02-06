# IdentificativoMovimentoModel

Dati di identificazione della registrazione tramite identificativo rilasciato dal RENTRI (da utilizzare in alternativa a anno di riferimento e progressivo)

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identificativo** | **str** | Identificativo RENTRI | 

## Example

```python
from rentri_dati_registri.models.identificativo_movimento_model import IdentificativoMovimentoModel

# TODO update the JSON string below
json = "{}"
# create an instance of IdentificativoMovimentoModel from a JSON string
identificativo_movimento_model_instance = IdentificativoMovimentoModel.from_json(json)
# print the JSON string representation of the object
print IdentificativoMovimentoModel.to_json()

# convert the object into a dict
identificativo_movimento_model_dict = identificativo_movimento_model_instance.to_dict()
# create an instance of IdentificativoMovimentoModel from a dict
identificativo_movimento_model_from_dict = IdentificativoMovimentoModel.from_dict(identificativo_movimento_model_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



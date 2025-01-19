# IdentificativoMovimentoCompletoModel

Dati di identificazione della registrazione con anno/progressivo e identificativo rilasciato dal RENTRI (modello utilizzato in output)

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**anno** | **int** | Anno di riferimento della registrazione | [optional] 
**progressivo** | **int** | Progressivo della registrazione | [optional] 
**identificativo** | **str** | Identificativo RENTRI | [optional] 

## Example

```python
from rentri_dati_registri.models.identificativo_movimento_completo_model import IdentificativoMovimentoCompletoModel

# TODO update the JSON string below
json = "{}"
# create an instance of IdentificativoMovimentoCompletoModel from a JSON string
identificativo_movimento_completo_model_instance = IdentificativoMovimentoCompletoModel.from_json(json)
# print the JSON string representation of the object
print(IdentificativoMovimentoCompletoModel.to_json())

# convert the object into a dict
identificativo_movimento_completo_model_dict = identificativo_movimento_completo_model_instance.to_dict()
# create an instance of IdentificativoMovimentoCompletoModel from a dict
identificativo_movimento_completo_model_from_dict = IdentificativoMovimentoCompletoModel.from_dict(identificativo_movimento_completo_model_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



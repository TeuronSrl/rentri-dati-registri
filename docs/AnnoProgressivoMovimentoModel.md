# AnnoProgressivoMovimentoModel

Dati di identificazione della registrazione tramite anno di riferimento e progressivo (da utilizzare in alternativa a identificativo rilasciato dal RENTRI)

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**anno** | **int** | Anno di riferimento della registrazione | 
**progressivo** | **int** | Progressivo della registrazione | 

## Example

```python
from rentri_dati_registri.models.anno_progressivo_movimento_model import AnnoProgressivoMovimentoModel

# TODO update the JSON string below
json = "{}"
# create an instance of AnnoProgressivoMovimentoModel from a JSON string
anno_progressivo_movimento_model_instance = AnnoProgressivoMovimentoModel.from_json(json)
# print the JSON string representation of the object
print(AnnoProgressivoMovimentoModel.to_json())

# convert the object into a dict
anno_progressivo_movimento_model_dict = anno_progressivo_movimento_model_instance.to_dict()
# create an instance of AnnoProgressivoMovimentoModel from a dict
anno_progressivo_movimento_model_from_dict = AnnoProgressivoMovimentoModel.from_dict(anno_progressivo_movimento_model_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



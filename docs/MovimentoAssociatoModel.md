# MovimentoAssociatoModel

Dati di identificazione della registrazione associata con anno/progressivo e identificativo rilasciato RENTRI (modello utilizzato in output)

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**anno** | **int** | Anno di riferimento della registrazione | [optional] 
**progressivo** | **int** | Progressivo della registrazione | [optional] 
**identificativo** | **str** | Identificativo RENTRI | [optional] 
**associazione_diretta** | **bool** | Specifica se l&#39;associazione della registrazione è stata comunicata durante la trasmissione dello stesso (true), oppure se è stata ricostruita in base a trasmissioni successive (false) | [optional] 
**incompleto** | **bool** | Specifica se della registrazione è incompleta (true), nel caso in cui sia stato derivato da un movimento associato trasmesso solamente come riferimento (anno/progressivo) di un altro movimento | [optional] 

## Example

```python
from rentri_dati_registri.models.movimento_associato_model import MovimentoAssociatoModel

# TODO update the JSON string below
json = "{}"
# create an instance of MovimentoAssociatoModel from a JSON string
movimento_associato_model_instance = MovimentoAssociatoModel.from_json(json)
# print the JSON string representation of the object
print(MovimentoAssociatoModel.to_json())

# convert the object into a dict
movimento_associato_model_dict = movimento_associato_model_instance.to_dict()
# create an instance of MovimentoAssociatoModel from a dict
movimento_associato_model_from_dict = MovimentoAssociatoModel.from_dict(movimento_associato_model_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



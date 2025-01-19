# DatiRiferimentiBaseModelRiferimentoOperazioneInner

Dati di identificazione della registrazione tramite anno di riferimento e progressivo oppure identificativo rilasciato dal RENTRI

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**anno** | **int** | Anno di riferimento della registrazione | 
**progressivo** | **int** | Progressivo della registrazione | 
**identificativo** | **str** | Identificativo RENTRI | 

## Example

```python
from rentri_dati_registri.models.dati_riferimenti_base_model_riferimento_operazione_inner import DatiRiferimentiBaseModelRiferimentoOperazioneInner

# TODO update the JSON string below
json = "{}"
# create an instance of DatiRiferimentiBaseModelRiferimentoOperazioneInner from a JSON string
dati_riferimenti_base_model_riferimento_operazione_inner_instance = DatiRiferimentiBaseModelRiferimentoOperazioneInner.from_json(json)
# print the JSON string representation of the object
print(DatiRiferimentiBaseModelRiferimentoOperazioneInner.to_json())

# convert the object into a dict
dati_riferimenti_base_model_riferimento_operazione_inner_dict = dati_riferimenti_base_model_riferimento_operazione_inner_instance.to_dict()
# create an instance of DatiRiferimentiBaseModelRiferimentoOperazioneInner from a dict
dati_riferimenti_base_model_riferimento_operazione_inner_from_dict = DatiRiferimentiBaseModelRiferimentoOperazioneInner.from_dict(dati_riferimenti_base_model_riferimento_operazione_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



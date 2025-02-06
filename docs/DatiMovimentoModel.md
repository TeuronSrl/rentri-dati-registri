# DatiMovimentoModel

Dati della registrazione (modello utilizzato in output)

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**riferimenti** | [**DatiRiferimentiCompletoModel**](DatiRiferimentiCompletoModel.md) | Riferimenti operazione | [optional] 
**rifiuto** | [**DatiRifiutoModel**](DatiRifiutoModel.md) | Identificazione del rifiuto.  Richiesto solamente se causale_operazione è diversa da \&quot;M\&quot;. | [optional] 
**materiali** | [**DatiMaterialiModel**](DatiMaterialiModel.md) | Materiali (solo impianti).  Richiesto solamente se causale_operazione è uguale a \&quot;M\&quot;. | [optional] 
**integrazione_fir** | [**DatiIntegrazioneFirModel**](DatiIntegrazioneFirModel.md) | Integrazione FIR - Registro C/S.  Non deve essere indicato se causale_operazione è diversa da \&quot;aT\&quot;, \&quot;TR\&quot;, \&quot;T*\&quot;, \&quot;T*AT\&quot;. | [optional] 
**esito** | [**DatiEsitoModel**](DatiEsitoModel.md) | Esito conferimento.  Non deve essere indicato se causale_operazione è diversa da \&quot;aT\&quot;, \&quot;T*AT\&quot;. | [optional] 
**produttore** | [**DatiProduttoreModel**](DatiProduttoreModel.md) | Produttore del rifiuto | [optional] 
**trasportatore** | [**DatiTrasportatoreModel**](DatiTrasportatoreModel.md) | Trasportatore | [optional] 
**destinatario** | [**DatiDestinatarioModel**](DatiDestinatarioModel.md) | Destinatario | [optional] 
**intermediario** | [**DatiIntermediarioModel**](DatiIntermediarioModel.md) | Intermediario     ⚠️ Deprecato: utilizzare \&quot;Intermediari\&quot; | [optional] 
**intermediari** | [**List[DatiIntermediarioModel]**](DatiIntermediarioModel.md) | Intermediari | [optional] 
**annotazioni** | **str** | Annotazioni generiche | [optional] 
**annullato** | **bool** | Indica se il movimento è annullato | [optional] 
**rettificato** | **bool** | Indica se il movimento è rettificato | [optional] 

## Example

```python
from rentri_dati_registri.models.dati_movimento_model import DatiMovimentoModel

# TODO update the JSON string below
json = "{}"
# create an instance of DatiMovimentoModel from a JSON string
dati_movimento_model_instance = DatiMovimentoModel.from_json(json)
# print the JSON string representation of the object
print DatiMovimentoModel.to_json()

# convert the object into a dict
dati_movimento_model_dict = dati_movimento_model_instance.to_dict()
# create an instance of DatiMovimentoModel from a dict
dati_movimento_model_from_dict = DatiMovimentoModel.from_dict(dati_movimento_model_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



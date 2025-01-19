# OperatoreIdentificativoRegistroMovimentiPostRequestInner

Dati della registrazione

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**riferimenti** | [**DatiRiferimentiBaseModel**](DatiRiferimentiBaseModel.md) | Riferimenti operazione | 
**rifiuto** | [**DatiRifiutoModel**](DatiRifiutoModel.md) | Identificazione del rifiuto.  Richiesto solamente se causale_operazione è diversa da \&quot;M\&quot;. | [optional] 
**materiali** | [**DatiMaterialiModel**](DatiMaterialiModel.md) | Materiali (solo impianti).  Richiesto solamente se causale_operazione è uguale a \&quot;M\&quot;. | [optional] 
**integrazione_fir** | [**DatiIntegrazioneFirModel**](DatiIntegrazioneFirModel.md) | Integrazione FIR - Registro C/S.  Non deve essere indicato se causale_operazione è diversa da \&quot;aT\&quot;, \&quot;TR\&quot;, \&quot;T*\&quot;, \&quot;T*AT\&quot;. | [optional] 
**esito** | [**DatiEsitoModel**](DatiEsitoModel.md) | Esito conferimento.  Non deve essere indicato se causale_operazione è diversa da \&quot;aT\&quot;, \&quot;T*AT\&quot;. | [optional] 
**produttore** | [**DatiProduttoreModel**](DatiProduttoreModel.md) | Produttore del rifiuto | [optional] 
**trasportatore** | [**DatiTrasportatoreModel**](DatiTrasportatoreModel.md) | Trasportatore | [optional] 
**destinatario** | [**DatiDestinatarioModel**](DatiDestinatarioModel.md) | Destinatario | [optional] 
**intermediario** | [**DatiIntermediarioModel**](DatiIntermediarioModel.md) | Intermediario     ⚠️ Deprecato: utilizzare \&quot;Intermediari\&quot; | [optional] 
**intermediari** | [**List[DatiIntermediarioModel]**](DatiIntermediarioModel.md) | Intermediari | [optional] 
**annotazioni** | **str** | Annotazioni contenenti il motivo dell&#39;annullamento | 
**numero_registrazione** | [**AnnoProgressivoMovimentoModel**](AnnoProgressivoMovimentoModel.md) | Numero registrazione della rettifica di annullamento tramite anno di riferimento e progressivo | 
**data_ora_registrazione** | **datetime** | Data di registrazione (formato ISO 8601 UTC) dell&#39;annullamento come previsto nel modello di registro RENTRI. Trattandosi di una registrazione informatica, è consentito indicare l&#39;ora, anche se non obbligatoria.  &lt;b&gt;Esempi:&lt;/b&gt; solo data &#x3D; \&quot;2024-01-01\&quot;, data con ora &#x3D; \&quot;2024-01-01T12:00:00Z\&quot; | 
**numero_registrazione_annullata** | [**OneOfAnnoProgressivoMovimentoModelIdentificativoMovimentoModel**](OneOfAnnoProgressivoMovimentoModelIdentificativoMovimentoModel.md) | Numero registrazione della registrazione da annullare | 

## Example

```python
from rentri_dati_registri.models.operatore_identificativo_registro_movimenti_post_request_inner import OperatoreIdentificativoRegistroMovimentiPostRequestInner

# TODO update the JSON string below
json = "{}"
# create an instance of OperatoreIdentificativoRegistroMovimentiPostRequestInner from a JSON string
operatore_identificativo_registro_movimenti_post_request_inner_instance = OperatoreIdentificativoRegistroMovimentiPostRequestInner.from_json(json)
# print the JSON string representation of the object
print(OperatoreIdentificativoRegistroMovimentiPostRequestInner.to_json())

# convert the object into a dict
operatore_identificativo_registro_movimenti_post_request_inner_dict = operatore_identificativo_registro_movimenti_post_request_inner_instance.to_dict()
# create an instance of OperatoreIdentificativoRegistroMovimentiPostRequestInner from a dict
operatore_identificativo_registro_movimenti_post_request_inner_from_dict = OperatoreIdentificativoRegistroMovimentiPostRequestInner.from_dict(operatore_identificativo_registro_movimenti_post_request_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



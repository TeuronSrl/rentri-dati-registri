# AnnullamentoMovimentoModel

Annullamento registrazione

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**numero_registrazione** | [**AnnoProgressivoMovimentoModel**](AnnoProgressivoMovimentoModel.md) | Numero registrazione della rettifica di annullamento tramite anno di riferimento e progressivo | 
**data_ora_registrazione** | **datetime** | Data di registrazione (formato ISO 8601 UTC) dell&#39;annullamento come previsto nel modello di registro RENTRI. Trattandosi di una registrazione informatica, è consentito indicare l&#39;ora, anche se non obbligatoria.  &lt;b&gt;Esempi:&lt;/b&gt; solo data &#x3D; \&quot;2024-01-01\&quot;, data con ora &#x3D; \&quot;2024-01-01T12:00:00Z\&quot; | 
**numero_registrazione_annullata** | [**OneOfAnnoProgressivoMovimentoModelIdentificativoMovimentoModel**](OneOfAnnoProgressivoMovimentoModelIdentificativoMovimentoModel.md) | Numero registrazione della registrazione da annullare | 
**annotazioni** | **str** | Annotazioni contenenti il motivo dell&#39;annullamento | 

## Example

```python
from rentri_dati_registri.models.annullamento_movimento_model import AnnullamentoMovimentoModel

# TODO update the JSON string below
json = "{}"
# create an instance of AnnullamentoMovimentoModel from a JSON string
annullamento_movimento_model_instance = AnnullamentoMovimentoModel.from_json(json)
# print the JSON string representation of the object
print(AnnullamentoMovimentoModel.to_json())

# convert the object into a dict
annullamento_movimento_model_dict = annullamento_movimento_model_instance.to_dict()
# create an instance of AnnullamentoMovimentoModel from a dict
annullamento_movimento_model_from_dict = AnnullamentoMovimentoModel.from_dict(annullamento_movimento_model_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



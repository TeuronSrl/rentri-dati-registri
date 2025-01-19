# DatiRiferimentiModel

Riferimenti dell'operazione

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**numero_registrazione** | [**AnnoProgressivoMovimentoModel**](AnnoProgressivoMovimentoModel.md) | Numero registrazione della registrazione tramite anno e progressivo | 
**data_ora_registrazione** | **datetime** | Data di registrazione (formato ISO 8601 UTC) come previsto nel modello di registro RENTRI. In caso di rettifica, è la data di registrazione della registrazione rettificata.  Trattandosi di una registrazione informatica, è consentito indicare l&#39;ora, anche se non obbligatoria.  &lt;b&gt;Esempi:&lt;/b&gt; solo data &#x3D; \&quot;2024-01-01\&quot;, data con ora &#x3D; \&quot;2024-01-01T12:00:00Z\&quot; | 
**causale_operazione** | [**CausaliOperazione**](CausaliOperazione.md) | Causale dell&#39;operazione.  Non richiesto solo nel caso di stoccaggio istantaneo (o giacenza).  Vedi API di codifica: &lt;i&gt;GET /codifiche/v1.0/causali-operazione&lt;/i&gt;&lt;p&gt;Valori ammessi:&lt;ul style&#x3D;\&quot;margin:0\&quot;&gt;&lt;li&gt;&lt;i&gt;DT&lt;/i&gt; - Prodotto o detenuto nell&#39;unità locale&lt;/li&gt;&lt;li&gt;&lt;i&gt;NP&lt;/i&gt; - Nuovo produttore&lt;/li&gt;&lt;li&gt;&lt;i&gt;T*&lt;/i&gt; - Ricevuto da terzi&lt;/li&gt;&lt;li&gt;&lt;i&gt;RE&lt;/i&gt; - Prodotto al di fuori dell’unità locale&lt;/li&gt;&lt;li&gt;&lt;i&gt;I&lt;/i&gt; - Scarico interno&lt;/li&gt;&lt;li&gt;&lt;i&gt;aT&lt;/i&gt; - Scarico a terzi&lt;/li&gt;&lt;li&gt;&lt;i&gt;M&lt;/i&gt; - Scarico per produzione di materiali&lt;/li&gt;&lt;li&gt;&lt;i&gt;TR&lt;/i&gt; - Intermediario&lt;/li&gt;&lt;li&gt;&lt;i&gt;T*aT&lt;/i&gt; - Carico e scarico&lt;/li&gt;&lt;/ul&gt;&lt;/p&gt; | [optional] 
**stoccaggio_istantaneo** | **datetime** | Data dello stoccaggio istantaneo (formato ISO 8601 UTC) (o giacenza), se valorizzata possono essere compilati solamente i dati relativi al rifiuto e non al materiale. | [optional] 
**numero_registrazione_rettifica** | [**DatiRiferimentiBaseModelNumeroRegistrazioneRettifica**](DatiRiferimentiBaseModelNumeroRegistrazioneRettifica.md) |  | [optional] 
**riferimento_operazione** | [**List[DatiRiferimentiBaseModelRiferimentoOperazioneInner]**](DatiRiferimentiBaseModelRiferimentoOperazioneInner.md) | Registrazioni associate | [optional] 

## Example

```python
from rentri_dati_registri.models.dati_riferimenti_model import DatiRiferimentiModel

# TODO update the JSON string below
json = "{}"
# create an instance of DatiRiferimentiModel from a JSON string
dati_riferimenti_model_instance = DatiRiferimentiModel.from_json(json)
# print the JSON string representation of the object
print(DatiRiferimentiModel.to_json())

# convert the object into a dict
dati_riferimenti_model_dict = dati_riferimenti_model_instance.to_dict()
# create an instance of DatiRiferimentiModel from a dict
dati_riferimenti_model_from_dict = DatiRiferimentiModel.from_dict(dati_riferimenti_model_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



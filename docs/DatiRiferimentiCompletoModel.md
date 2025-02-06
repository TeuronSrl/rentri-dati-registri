# DatiRiferimentiCompletoModel

Riferimenti dell'operazione (modello utilizzato in output)

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**numero_registrazione** | [**IdentificativoMovimentoCompletoModel**](IdentificativoMovimentoCompletoModel.md) | Numero registrazione della registrazione tramite anno e progressivo e identificativo rilasciato dal RENTRI | [optional] 
**data_ora_registrazione** | **datetime** | Data di registrazione (formato ISO 8601 UTC) come previsto nel modello di registro RENTRI. In caso di rettifica, è la data di registrazione della registrazione rettificata.  Trattandosi di una registrazione informatica, è consentito indicare l&#39;ora, anche se non obbligatoria.  &lt;b&gt;Esempi:&lt;/b&gt; solo data &#x3D; \&quot;2024-01-01\&quot;, data con ora &#x3D; \&quot;2024-01-01T12:00:00Z\&quot; | 
**numero_registrazione_di_rettifica** | [**IdentificativoMovimentoCompletoModel**](IdentificativoMovimentoCompletoModel.md) | Numero della registrazione della rettifica | [optional] 
**numero_registrazione_rettifica** | [**IdentificativoMovimentoCompletoModel**](IdentificativoMovimentoCompletoModel.md) | Numero della registrazione rettificata | [optional] 
**causale_operazione_cs** | [**CausaliOperazioneCs**](CausaliOperazioneCs.md) | Causale dell&#39;operazione Carico/Scarico&lt;p&gt;Valori ammessi:&lt;ul style&#x3D;\&quot;margin:0\&quot;&gt;&lt;li&gt;&lt;i&gt;Carico&lt;/i&gt; - Carico&lt;/li&gt;&lt;li&gt;&lt;i&gt;Scarico&lt;/i&gt; - Scarico&lt;/li&gt;&lt;li&gt;&lt;i&gt;CaricoScarico&lt;/i&gt; - Carico e scarico&lt;/li&gt;&lt;/ul&gt;&lt;/p&gt; | [optional] 
**causale_operazione** | [**CausaliOperazione**](CausaliOperazione.md) | Causale dell&#39;operazione.  Non richiesto solo nel caso di stoccaggio istantaneo (o giacenza).  Vedi API di codifica: &lt;i&gt;GET /codifiche/v1.0/causali-operazione&lt;/i&gt;&lt;p&gt;Valori ammessi:&lt;ul style&#x3D;\&quot;margin:0\&quot;&gt;&lt;li&gt;&lt;i&gt;DT&lt;/i&gt; - Prodotto o detenuto nell&#39;unità locale&lt;/li&gt;&lt;li&gt;&lt;i&gt;NP&lt;/i&gt; - Nuovo produttore&lt;/li&gt;&lt;li&gt;&lt;i&gt;T*&lt;/i&gt; - Ricevuto da terzi&lt;/li&gt;&lt;li&gt;&lt;i&gt;RE&lt;/i&gt; - Prodotto al di fuori dell’unità locale&lt;/li&gt;&lt;li&gt;&lt;i&gt;I&lt;/i&gt; - Scarico interno&lt;/li&gt;&lt;li&gt;&lt;i&gt;aT&lt;/i&gt; - Scarico a terzi&lt;/li&gt;&lt;li&gt;&lt;i&gt;M&lt;/i&gt; - Scarico per produzione di materiali&lt;/li&gt;&lt;li&gt;&lt;i&gt;TR&lt;/i&gt; - Intermediario&lt;/li&gt;&lt;li&gt;&lt;i&gt;T*aT&lt;/i&gt; - Carico e scarico&lt;/li&gt;&lt;/ul&gt;&lt;/p&gt; | [optional] 
**stoccaggio_istantaneo** | **datetime** | Data dello stoccaggio istantaneo (formato ISO 8601 UTC) (o giacenza), se valorizzata possono essere compilati solamente i dati relativi al rifiuto e non al materiale. | [optional] 
**riferimenti_operazione** | [**List[MovimentoAssociatoModel]**](MovimentoAssociatoModel.md) | Registrazioni associate     ⚠️ Deprecato: utilizzare \&quot;riferimento_operazione\&quot; | [optional] [readonly] 
**riferimento_operazione** | [**List[MovimentoAssociatoModel]**](MovimentoAssociatoModel.md) | Registrazioni associate | [optional] [readonly] 
**identificativo_registro** | **str** | Identificativo del registro | [optional] 
**num_iscr_sito** | **str** | Numero iscrizione unità locale rilasciato all&#39;iscrizione | [optional] 
**data_creazione** | **datetime** | Data di creazione della registrazione in RENTRI (formato ISO 8601 UTC) | [optional] 
**data_trasmissione** | **datetime** | Data di trasmissione della registrazione a RENTRI (formato ISO 8601 UTC) | [optional] 
**data_inizio_validita** | **datetime** | Data di inizio validità della posizione (formato ISO 8601 UTC) | [optional] 
**data_fine_validita** | **datetime** | Data di fine validità della posizione (formato ISO 8601 UTC) | [optional] 

## Example

```python
from rentri_dati_registri.models.dati_riferimenti_completo_model import DatiRiferimentiCompletoModel

# TODO update the JSON string below
json = "{}"
# create an instance of DatiRiferimentiCompletoModel from a JSON string
dati_riferimenti_completo_model_instance = DatiRiferimentiCompletoModel.from_json(json)
# print the JSON string representation of the object
print DatiRiferimentiCompletoModel.to_json()

# convert the object into a dict
dati_riferimenti_completo_model_dict = dati_riferimenti_completo_model_instance.to_dict()
# create an instance of DatiRiferimentiCompletoModel from a dict
dati_riferimenti_completo_model_from_dict = DatiRiferimentiCompletoModel.from_dict(dati_riferimenti_completo_model_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



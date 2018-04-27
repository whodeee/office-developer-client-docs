---
title: "OriginalValue Property (ADO)"
 
 
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
  
localization_priority: Normal
ms.assetid: 02ffc728-4692-d439-e2a6-2f02cca53a71

---

# OriginalValue Property (ADO)

Indicates the value of a [Field](field-object-ado.md) that existed in the record before any changes were made. 
  
## Return Value

Returns a **Variant** value that represents the value of a field prior to any change. 
  
## Remarks

Use the **OriginalValue** property to return the original field value for a field from the current record. 
  
In  *immediate update mode*  (in which the provider writes changes to the underlying data source after you call the [Update](update-method-ado.md) method), the **OriginalValue** property returns the field value that existed prior to any changes (that is, since the last **Update** method call). This is the same value that the [CancelUpdate](cancelupdate-method-ado.md) method uses to replace the [Value](value-property-ado.md) property. 
  
In  *batch update mode*  (in which the provider caches multiple changes and writes them to the underlying data source only when you call the [UpdateBatch](updatebatch-method-ado.md) method), the **OriginalValue** property returns the field value that existed prior to any changes (that is, since the last **UpdateBatch** method call). This is the same value that the [CancelBatch](cancelbatch-method-ado.md) method uses to replace the **Value** property. When you use this property with the [UnderlyingValue](underlyingvalue-property-ado.md) property, you can resolve conflicts that arise from batch updates. 
  
## Record

For [Record](record-object-ado.md) objects, the **OriginalValue** property will be empty for fields added before [Update](update-method-ado.md) is called. 
  

---
title: "Açık bir iş listesinde sistem gruplama"
description: "Bu konu, mobil cihazda açık iş listesine nasıl filtre uygulanacağını açıklar."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0c68d544fec985f325e6472203533f23948cc9b4
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="system-grouping-on-an-open-work-list"></a>Açık bir iş listesinde sistem gruplama

[!include[banner](../includes/banner.md)]

Sistem gruplandırma alanını kullanarak, mobil cihaz menü öğesini düzenlemek zorunda kalmadan bir açık iş listesini filtreleyebilirsiniz.
Bu geçerli olduğunda, sistem gruplandırma, tek bir iş başlığı alanındaki bir iş listesini filtrelemek üzere çalışır. Sistem gruplandırmayı satır düzeyindeki alanlarda filtreleme yapmak için kullanamazsınız.

## <a name="set-up-system-grouping-on-an-open-work-list"></a>Açık bir iş listesinde sistem gruplandırmayı ayarlama
Açık bir iş listesinde sistem gruplandırmayı ayarlamak için aşağıdaki adımları uygulayın.

-   Bir mobil cihaz menü öğesinden **Mod: Dolaylı** ve **Faaliyet Kodu: Açık iş listesini görüntüle**'yi seçin. Aşağıdaki seçenekler kullanılabilir olur. Bu seçenekler bir açık iş listesinde sistem gruplandırması için gereklidir. 

| Seçenek        | Açıklama   | 
| ------------- | ------------- |
| Sistem gruplandırmaya izin ver   | Seçili iş listesi menü öğesi için sistem gruplandırmayı etkinleştirir.| 
| Sistem gruplandırma alanı   | Yalnızca **Sistem işine izin ver** **Evet** olarak ayarlandığında kullanılabilir. Çalışanlar için çekme işinin nasıl gruplanacağını belirleyen bu alanı seçin. Örneğin, **ShipmentId** alanını seçerseniz çalışan çekme işini gruplandırmak için sevkıyat kodunu tarayacaktır. Böylece sevkıyat için tüm iş çalışana atanır. Bu alan, sistem tarafından gruplanan mevcut işi kullanmak için bir menü öğesi oluşturmanızı gerektirir. Çalışanı neyi taraması gerektiği hakkında bilgilendirmek için **Sistem gruplandırma etiketi** alanını kullanın. |
| Sistem gruplandırma etiketi   | Yalnızca **Sistem işine izin ver** **Evet** olarak ayarlandığında kullanılabilir. Çalışan için çekme işi gruplandırma sırasında neyin taranacağına ilişkin bilgileri girin. Örneğin çekme işini sevkiyata göre gruplandırmak için **ShipmentId** alanını kullanıyorsanız alana Sevkiyat kodu girebilirsiniz. Bu alan, sistem tarafından gruplanan mevcut işi kullanmak için bir menü öğesi oluşturmanızı gerektirir. **Sistem gruplandırma** alanında alanı nasıl gruplandıracağınızı da seçmelisiniz.|


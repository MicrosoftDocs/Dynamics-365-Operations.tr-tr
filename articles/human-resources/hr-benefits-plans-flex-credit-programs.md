---
title: Esnek kredi programları ayarlama
description: Çalışanları, önceden belirlenmiş esnek kredi sayısına göre sosyal haklar kaydetmek için, Microsoft Dynamics 365 Human Resources'un esnek kredi programlarını kullanabilirsiniz.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitCreditPrograms
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d27d0f7f3f7e7db62b5d46b3b689d11194a85253
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010879"
---
# <a name="set-up-flex-credit-programs"></a>Esnek kredi programları ayarlama

[!include [banner](includes/preview-feature.md)]

Çalışanları, önceden belirlenmiş esnek kredi sayısına göre sosyal haklar kaydetmek için, Microsoft Dynamics 365 Human Resources'un esnek kredi programlarını kullanabilirsiniz. Çalışanlar esnek kredileri nasıl tahsis etmek için seçim yapabilir. Örneğin, bir çalışanın eşinin sağlık durumu planı kapsamında olması durumunda, diğer avantajlara doğru, sistem durumu kapsamında kullanılmasını istedikleri kredileri kullanmak isteyebilir. 

1. **Sosyal haklar** yönetimi çalışma alanında, **Planlar** altında, **Esnek kredi programları**'nı seçin.

2. **Yeni**'yi seçin.

3. Aşağıdaki alanların değerleri belirtin:

   | Alan | Tanım |
   | --- | --- |
   | Kazanç kredisi kodu | Esnek kredi programının benzersiz tanımlayıcısı. |
   | Tanım | Esnek kredi programı açıklaması. | 
   | Başlangıç tarihi | Esnek kredi programının etkin olacağı tarih. |
   | Bitiş tarihi | Esnek kredi programının son tarihi. Esnek kredi programının zamanlanan bir sona erme tarihi olmadığını belirtmek için varsayılan değeri (12/31/2154) boş bırakabilirsiniz. |
   | Toplam Kredi Değeri | Her çalışanın avantajları için kullanması gerekecektir kullanılan alacak sayısı. |
   | Eşit Dağıtma Kuralı | Esnek kredi dönemi ortasında bir çalışan işe alındığında, esnek krediler için kullanılacak kural. </br></br><ul><li>**Hiçbiri** – esnek kredi programı başlatıldıktan sonra işe alındığında çalışan esnek kredi almaz.</li><li>**Tam kredi** – çalışan, işe alındıklarında bağımsız olarak, tüm esnek kredi tutarını alır.</li><li>**Eşit dağıt** – çalışan, başlangıç tarihlerine göre eşit miktarda esnek kredi alır.</li></ul> |
   | Esnek Kredi Eşit Dağıtma Formülü | Esnek kredi programının kazanç dönemi ortasında bir çalışan işe alındığında, esnek krediler için kullanılacak kural. Kat, istihdam başlangıç tarihine dayanır. Bu alan yalnızca **eşit dağıtma kural**ı alanında **eşit dağıt** seçeneği seçildiğinde kullanılır. </br></br><ul><li>**Günlük** – bir çalışanın gün düzeyine alacağı esnek kredi sayısı. Esnek kredi toplam sayısı dönem içindeki gün sayısına bölünür. Örneğin, bir avantaj dönemi 400 gün ise, sistem günde alınan esnek kredi sayısını hesaplamak üzere, toplam esnek kredi sayısını 400 ile bölecektir.</li><li>**Geçerli ay** - Bir çalışanın geçerli aya yuvarlanmış, ay düzeyine aldığı esnek kredi sayısı. Esnek kredi toplam sayısı dönem içindeki ay sayısına bölünür. Örneğin, bir avantaj dönemi 15 ay ise, sistem ayda alınan esnek kredi sayısını hesaplamak üzere, toplam esnek kredi sayısını 15 ile bölecektir.</li><li>**Sonraki ay** - Bir çalışanın sonraki aya yuvarlanmış, ay düzeyine aldığı esnek kredi sayısı. Esnek kredi toplam sayısı dönem içindeki ay sayısına bölünür. Örneğin, bir avantaj dönemi 15 ay ise, sistem ayda alınan esnek kredi sayısını hesaplamak üzere, toplam esnek kredi sayısını 15 ile bölecektir.</li></ul> |
   

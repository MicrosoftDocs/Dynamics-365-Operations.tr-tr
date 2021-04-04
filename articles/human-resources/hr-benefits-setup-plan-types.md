---
title: Plan türleri oluşturma
description: Microsoft Dynamics 365 Human Resources'ta plan tipi belirli avantaj tiplerinin üst düzey gruplandırmasıdır. Her plan türü, plan türüyle ilgili kuralları belirleyen bir plan türü koduna sahiptir.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1d8db6900e6b697e988e2a7e9e31828b70e4ad0d
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463924"
---
# <a name="create-plan-types"></a>Plan türleri oluşturma

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resources'ta plan tipi belirli avantaj tiplerinin üst düzey gruplandırmasıdır. Her plan türü, plan türüyle ilgili kuralları belirleyen bir plan türü koduna sahiptir. Örneğin, temel kullanım plan türü, bir çeşit ömür iş sigortası planı olduğundan ve ömür planı türü kodu için oluşturulan kurallara uygun olması gereken plan türü kodu ömrüne sahip olacaktır. Başka bir plan türü, planlama türü kod ömrü ile aynı zamanda ek ömür olabilir.

Her plan tipi bir çalışanın türünün veya birden fazla bir plana kayıt yapıp kaydedemeyeceğini gösterir. Örneğin, bir çalışan plan türü ömrü ile ilgili temel ömür ve ek kullanım ömrü ilkelerine kayıt yapabilir. Bir çalışanın büyük olasılıkla tıbbi tip bir ilkeye kaydetmesine izin verilir.

Bir plan türü ilgili kişiler içeriyorsa, plan türü ilgili kişilerin lehdar veya bağımlı olup olmadığını gösterir. Örneğin, temel bir ömür planı türü, temel bir tıbbi plan türünün bağımlıları olması halinde lehsiz olurdu. Bazı durumlarda, bir planın kişisel ilgili kişisi olmayabilir. Örneğin, esnek bir harcama hesabı veya Park kesintisi.

Plan türü, kapsam seçeneklerini tanımlayabilir. Kapsam seçenekleri, kapsma seçeneği formunda tanımlanmıştır. Tedarik seçeneği, plan türüne uygun olan kazancın veya ilgili kişilerin tutarını belirtebilir. Örneğin, ilgili kişi türü lehdar ise, kapsam seçeneği, lehdar kullanıldığında kazancın ne kadar uygun olacağını tanımlamalıdır. İlgili kişi türü bağımlı ise, kapsam seçeneğinin bağımlı ve çalışan arasındaki ilişkiyi tanımlaması gerekir. 

1. **Sosyal haklar** yönetimi çalışma alanında, **Kur** altında, **Plan türleri**'nı seçin.

2. **Yeni**'yi seçin.

3. Aşağıdaki alanların değerleri belirtin:

   | Alan | Tanım |
   | --- | --- |
   | **Plan türü** | Plan türünü tanımlayan benzersiz ad. |
   | **Açıklama** | PLan türü açıklaması. |
   | **Plan türü kodu** | Açılan değerler listesinden bir plan türü kodu seçin. Plan türü kod listesi, geçerli sürümde desteklenen tüm plan tiplerini görüntüler. |
   | **Eş zamanlı kayıt** | Bir çalışanın aynı plan türünde çoklu kazanç planlarına veya her plan türü başına yalnızca bir avantaj planına kayıt yapıp kullanamayacağını belirtir. |
   | **İlgili kişi türü** | Kişisel ilgili kişinin rolünü belirtir. Değerler boş, bağımlı ve lehdar değerlerdir. Plan tiplerinde kapsam seçeneğine dayalı olarak bir bağımlı veya lehdar gerekmiyorsa, **İlgili kişi türü**'nü boş bırakabilirsiniz. |

4. Ömür olayı seçeneklerini yapılandırmak için, **eylemler**'i seçin ve sonra da **ömür olayı seçenekleri**'ni seçin. Aşağıdaki alanların değerleri belirtin:

   | Alan | Tanım |
   | --- | --- |
   | **Plan türü** | Ömür olayı seçeneklerini konfigüre etmek için plan türü. |
   | **Yaşam olayı tür kodu** | Ömür olayı türünün kodu. |
   | **İptale izin ver** | Bir çalışanın ömür olayı sırasında bir sosyal haklar planını iptal edip kullanamayacağını belirtir. |
   | **Karşılama seçeneğini değiştir** | Bir çalışanın ömür olayı sırasında bir kapsam seçeneklerini değiştirip değiştiremeyeceğini belirtir. |
   | **Yeni bir plana geç** | Bir çalışanın ömür olayı sırasında planlarını değiştirip değiştiremeyeceğini belirtir. |
   | **Planı otomatik olarak iptal et** | Ömür olayı sırasında planın otomatik olarak iptal edip edilmeyeceğini belirtir. |
   | **Uygunluk denetimini otomatik olarak yeniden aç** | Yaşam olayı sırasında kazanç kaydı uygunluk denetiminin otomatik olarak yeniden açılıp açılmayacağını belirtir. |
   | **Raporlama aralığı** | Yaşam olayının raporlama aralığını gün olarak belirtir. **Not**: tutar girmezseniz, sistem raporlama penceresinin sıfır olmasını varsayar ve ömür olayını işlemez. |

5. **Kaydet**'i seçin. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
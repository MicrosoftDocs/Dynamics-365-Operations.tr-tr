---
title: Plan türüne genel bakış
description: Microsoft Dynamics 365 Human Resources'ta plan tipi belirli avantaj tiplerinin üst düzey gruplandırmasıdır. Her plan türü, plan türüyle ilgili kuralları belirleyen bir plan türü koduna sahiptir.
author: andreabichsel
ms.date: 06/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 806b3839feb1e1bf889747986388a56113c3ebe1
ms.sourcegitcommit: 08797bc43e93ea05711c5a70dd7cdb82cada667a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/13/2021
ms.locfileid: "6558285"
---
# <a name="plan-type-overview"></a>Plan türüne genel bakış

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Plan tipi belirli avantaj tiplerinin üst düzey gruplandırmasıdır. Her plan türü, plan türüyle ilgili kuralları belirleyen bir plan türü koduna sahiptir. Örneğin, **Temel yaşam** planı türü, bir tür hayat sigortası planı olduğundan ve **Yaşam** planı türü kodu için oluşturulmuş kurallara uyması gerektiğinden, **Yaşam** planı türü koduna sahip olacaktır. Başka bir plan türü **Ek yaşam** olabilir. Bu plan türü, **Yaşam** planı türü koduna da sahip olacaktır.

Her plan tipi bir çalışanın türünün veya birden fazla bir plana kayıt yapıp kaydedemeyeceğini gösterir. Örneğin, bir çalışan plan türü ömrü ile ilgili temel ömür ve ek kullanım ömrü ilkelerine kayıt yapabilir. Bir çalışanın büyük olasılıkla tıbbi tip bir ilkeye kaydetmesine izin verilir.

Bir plan türü ilgili kişiler içeriyorsa, plan türü ilgili kişilerin lehdar veya bağımlı olup olmadığını gösterir. Örneğin, temel bir ömür planı türü, temel bir tıbbi plan türünün bağımlıları olması halinde lehsiz olurdu. Bazı durumlarda, bir planın kişisel ilgili kişisi olmayabilir. Örneğin, esnek bir harcama hesabı veya Park kesintisi.

Plan türü, kapsam seçeneklerini tanımlayabilir. Kapsam seçenekleri, kapsma seçeneği formunda tanımlanmıştır. Tedarik seçeneği, plan türüne uygun olan kazancın veya ilgili kişilerin tutarını belirtebilir. Örneğin, ilgili kişi türü lehdar ise, kapsam seçeneği, lehdar kullanıldığında kazancın ne kadar uygun olacağını tanımlamalıdır. İlgili kişi türü bağımlı ise, kapsam seçeneğinin bağımlı ve çalışan arasındaki ilişkiyi tanımlaması gerekir. 

> [!IMPORTANT]
> Form, yeni bir avantaj planı oluşturulduğunda kullanılabilen seçenekleri etkileyen önemli verileri içerir:
>
> - **Plan türü kodu**: Bu alan, gerçek yan hak ayarlandığında **Yapılandırma** sekmesinde gösterilenleri etkiler.  
> - **Eşzamanlı kayıt**: Bu alan, birden çok kayda izin verilip verilmeyeceğini belirler. (Tıbbi bir plan için bu alan genellikle **Bir kayıt** olarak ayarlanır.)
> - **İlgili kişi türü**: Bu alan, bakmakla yükümlü olunan kişileri veya yararlananları bir plana eklemeyi sağlar. **Hiçbiri** olarak ayarlanırsa yan haklara kaydedilen çalışanlar bir yararlanan veya bakmakla yükümlü olunan kişi seçme seçeneğine sahip olmaz.
> - **Kapsam seçenekleri**: Kapsam seçeneklerini plan türleriyle ilişkilendirmek için bu alanı kullanın. Bu plan türü kapsamında olacak bireyleri veya bu plan türü için kullanılabilir kapsam tutarlarını tanımlar. Örneğin, bir tıbbi plan türü için kapsamın yalnızca çalışan, çalışan ve başka bir kişi veya çalışan ve ailesi için kullanılabileceğini belirtebilirsiniz.

## <a name="create-plan-types"></a>Plan türleri oluşturma

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

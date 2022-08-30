---
title: Plan türüne genel bakış
description: Microsoft Dynamics 365 Human Resources'ta plan tipi belirli avantaj tiplerinin üst düzey gruplandırmasıdır.
author: twheeloc
ms.date: 08/24/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6ca14156c165ca3f536fc0120ebd03883284eb18
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337075"
---
# <a name="plan-type-overview"></a>Plan türüne genel bakış

[!include [banner](../includes/preview-banner.md)]

Plan tipi belirli avantaj tiplerinin üst düzey gruplandırmasıdır. Her plan türü, plan türüyle ilgili kuralları belirleyen bir plan türü koduna sahiptir. Örneğin, **Temel yaşam** planı türü, bir tür hayat sigortası planı olduğundan ve **Yaşam** planı türü kodu için oluşturulmuş kurallara uyması gerektiğinden, **Yaşam** planı türü koduna sahip olacaktır. Başka bir plan türü **Ek yaşam** olabilir. Bu plan türü, **Yaşam** planı türü koduna da sahip olacaktır.

Her plan tipi bir çalışanın türünün veya birden fazla bir plana kayıt yapıp kaydedemeyeceğini gösterir. Örneğin, bir çalışan plan türü ömrü ile ilgili **Temel ömür** ve **Ek kullanım ömrü** ilkelerine kayıt yapabilir. Bir çalışanın büyük olasılıkla tıbbi tip bir ilkeye kaydetmesine izin verilir.

Bir plan türü ilgili kişiler içeriyorsa, plan türü ilgili kişilerin lehdar veya bağımlı olup olmadığını gösterir. Örneğin, temel bir tıbbi plan türünün bağımlıları varken **Temel ömür** plan türünün lehtarları olurdu. Bazı durumlarda, bir planın kişisel ilgili kişisi olmayabilir. Örneğin, esnek bir harcama hesabı veya Park kesintisi.


Plan türü, kapsam seçeneklerini tanımlayabilir. Kapsam seçenekleri **Kapsam seçenekleri** sayfasında tanımlanır. Tedarik seçeneği, plan türüne uygun olan kazancın veya ilgili kişilerin tutarını belirtebilir. Örneğin, ilgili kişi türü **Lehdar** ise kapsam seçeneği, kazanç kullanıldığında lehdarın ne kadar uygun olacağının koşullarını tanımlamalıdır. İlgili kişi türü **Bağımlı** ise kapsam seçeneğinin bağımlı ve çalışan arasındaki ilişkiyi tanımlaması gerekir. 

> [!IMPORTANT]
> **Plan türleri** sayfası, yeni bir kazanç planı oluşturulduğunda kullanılabilen seçenekleri etkileyen temel verileri içerir:
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
   | **Karşılama seçeneğini değiştir** | Bir çalışanın ömür olayı sırasında bir kapsam seçeneklerini değiştirip değiştiremeyeceğini belirtir. |
   | **Yeni bir plana geç** | Bir çalışanın ömür olayı sırasında planlarını değiştirip değiştiremeyeceğini belirtir. |
   | **Uygunluk denetimini otomatik olarak yeniden aç** | Yaşam olayı sırasında kazanç kaydı uygunluk denetiminin otomatik olarak yeniden açılıp açılmayacağını belirtir. |
   | **Yaşam olayı kayıt dönemi** | Yaşam olayının raporlama aralığını gün olarak belirtir. **Not**: tutar girmezseniz, sistem raporlama penceresinin sıfır olmasını varsayar ve ömür olayını işlemez. |
   | **Yalnızca yönetici tarafından düzenlenebilir** | Bir yöneticinin bir yaşam olayı sırasında bir planı iptal edip edemeyeceğini veya düzenleyip düzenleyemeyeceğini belirtir. Çalışan tarafından **Personel self servisi** çalışma alanında hiçbir değişiklik yapılamaz. |
   | **Planı otomatik olarak iptal et** | Yaşam olayı sırasında planın otomatik olarak iptal edilmesi gerekip gerekmediğini belirtir. Yaşam olayı değişiklikleri işlendikten sonra, **Planı otomatik olarak iptal et** seçeneği plan seçimini korur. Yalnızca **Onaylandı** veya **Kullanıma alındı** durumu kaldırılacaktır. Plan seçili olarak kalır. Bu nedenle, plan seçimlerini yaşam olayı kayıt süresi içinde yapmayan çalışanlar, plan seçimini kaybetmez. 

5. **Kaydet**'i seçin. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]

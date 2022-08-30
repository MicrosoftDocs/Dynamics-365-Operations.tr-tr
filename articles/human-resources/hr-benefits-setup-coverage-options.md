---
title: Kapsam seçeneklerini oluşturma
description: Bu makalede, bir kazanç planında veya programında bir katılımcının seçilmesi için Microsoft Dynamics 365 Human Resources'daki kapsam seçenekleri açıklanmaktadır.
author: twheeloc
ms.date: 08/24/2021
ms.topic: article
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
ms.openlocfilehash: f9c107e31e58ba1302cd02e2e82aa405dda0fdef
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337090"
---
# <a name="create-coverage-options"></a>Kapsam seçeneklerini oluşturma


Kapsam seçenekleri, sigorta planında kimlerin kapsanması gerektiğini veya ne kadar teminat olduğunu belirler. Örneğin, bir tıbbi plan için **Yalnızca çalışan** seçeneği, **Çalışan + 1** seçeneği ve **Aile** seçeneğiniz olabilir. Hayat sigortası için **1 x maaş** veya **2 x maaş** için teminat sunabilirsiniz.

Yan hak teminatı seçenekleri tanımlandıktan sonra bunları yeniden kullanabilirsiniz. Bir seçeneği bir veya daha fazla planla ilişkilendirebilirsiniz.

> [!IMPORTANT]
> Teminat seçeneklerini tanımladıktan sonra, bunları bir yan hak planı türüne ekleyin. Plan türü daha sonra bir kazanç planıyla veya programla ilişkilendirilir. Bir plan türüyle ilişkili teminat seçenekleri, oluşturulan bu türdeki tüm planlar tarafından kullanılabilir.

## <a name="create-coverage-options"></a>Kapsam seçeneklerini oluşturma
1. **Sosyal haklar** yönetimi çalışma alanında, **Kur** altında, **Kapsam seçenekler**'i seçin.

2. **Yeni**'yi seçin.

3. Aşağıdaki alanların değerleri belirtin:

   | Alan | Tanım |
   | --- | --- |
   | **Karşılama seçeneği** | Benzersiz bir karşılama seçeneği adı. |
   | **Açıklama** | Kapsam seçeneği için bir açıklama girin. |
   | **Karşılama kodu** | Karşılama kodları, uygun olan her kişi türü için minimum ve maksimum tutarları atar. Bir karşılama kodu, bir plan türü için izin verilen kapsam miktarını veya kapsamayı gösterir. Tedarik tutarını YTL tutarı veya yüzde olarak ifade edebilirsiniz. Örneğin:<ul><li>**Çalışan+1** – nitelikli olması için çalışanın bir bağımlı seçili olması gerekir (birden fazla seçili ise, artık uygun olmayacaktır).</li><li>**Çalışan + aile** – nitelikli olması için çalışanın en az iki yanındaki seçilmiş olması gerekir.</li></ul> |
   | **Maksimum sayı** | Maksimum bağımlı sayısı |
   | **Durum** | Kapsam seçeneği durumu. Kapsam seçeneğinin durumu **Etkin Değil** olarak ayarlandıysa Kapsam seçeneği plan türlerinde seçilemez. |
   | **Yüzde** | Yüzde tutarı. Bu alan yalnızca, Kapsam kodu alanında % x maaş seçilmişse etkindir. |
   | **Bölen** | % X maaş kapsam kodunu seçtiğinizde hesaplamada kullanılacak bölen. |
   | **Minimum yüzde** | Yüzde kapsam kodunu seçtiğinizde minimum yüzde. |
   | **Maksimum yüzde** | Yüzde kapsam kodunu seçtiğinizde maksimum yüzde. |

4. **Kişisel ilgili kişi uygunluğu seçenekleri** altında, her kapsam seçeneğine uygun özel ilgili kişiler uygunluk seçeneğini ekleyin.

5. **Self servis** altında, aşağıdaki alanların değerleri belirtin:

   | Alan | Tanım |
   | --- | --- |
   | **Personel katkı tutarına izin ver** | Çalışanların kazançları seçtiklerinde Kazançlar self servisindeki katkı tutarını değiştirmelerine izin verilip verilmeyeceğini belirtir. Bu onay kutusunu seçerseniz sistem, çalışanın Kazançlar self servise girdiği katkı tutarına göre kazanç planı parametrelerini hesaplar. |
   | **Personel karşılama tutarına izin ver** | Çalışanların, sosyal hakları seçtiklerinde Kazançlar self servisteki kapsam tutarını değiştirmelerine izin verilip verilmeyeceğini belirtir. Bu onay kutusunu seçerseniz, sistem, personel self servis üzerine girdiği kapsam tutarını temel alarak, kazanç planı parametrelerini hesaplar. |

6. **Kaydet**'i seçin. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]

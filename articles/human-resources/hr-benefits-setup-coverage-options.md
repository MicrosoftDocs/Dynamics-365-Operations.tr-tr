---
title: Kapsam seçeneklerini oluşturma
description: Microsoft Dynamics 365 Human Resources'taki karşılama seçenekleri, bir kazanç planında veya programında bir katılımcının seçimi için kapsam düzeyleridir.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 021fea7604af2fff833ddc6868d55a316ef70aae
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/06/2020
ms.locfileid: "3230189"
---
# <a name="create-coverage-options"></a>Kapsam seçeneklerini oluşturma

Microsoft Dynamics 365 Human Resources'taki karşılama seçenekleri, bir kazanç planında veya programında bir katılımcının seçimi için kapsam düzeyleridir. Örneğin, kapsam seçenekleri tıbbi bir plan için **Yalnızca Personel** veya bir hayat sigortası planı için **2x Maaş** içerebilir. Tanımlandıktan sonra, kazanç kapsamı seçeneklerini yeniden kullanabilirsiniz. Bir seçeneği bir veya daha fazla planla ilişkilendirebilirsiniz.

Kapsam seçeneklerini tanımladıktan sonra, karşılama seçeneklerini bir kazanç planı türüne ekleyin. Plan türü daha sonra bir kazanç planıyla veya programla ilişkilendirilir. Bir plan tipiyle ilişkilendirilmiş olan kapsam seçenekleri, bu plan türü ile oluşturulan tüm planlar tarafından kullanılabilir. 

1. **Sosyal haklar** yönetimi çalışma alanında, **Kur** altında, **Kapsam seçenekler**'i seçin.

2. **Yeni**'yi seçin.

3. Aşağıdaki alanların değerleri belirtin:

   | Alan | Tanım |
   | --- | --- |
   | **Karşılama seçeneği** | Benzersiz bir karşılama seçeneği adı. |
   | **Açıklama** | Kapsam seçeneği için bir açıklama girin. |
   | **Karşılama kodu** | Karşılama kodları, uygun olan her kişi türü için minimum ve maksimum tutarları atar. Bir karşılama kodu, bir plan türü için izin verilen kapsam miktarını veya kapsamayı gösterir. Tedarik tutarını YTL tutarı veya yüzde olarak ifade edebilirsiniz. Örneğin:</br></br>- **Çalışan+1** – nitelikli olması için çalışanın bir bağımlı seçili olması gerekir (birden fazla seçili ise, artık uygun olmayacaktır).</br></br>- **Çalışan + aile** – nitelikli olması için çalışanın en az iki yanındaki seçilmiş olması gerekir. |
   | **Maksimum sayı** | Maksimum bağımlı sayısı |
   | **Durum** | Kapsam seçeneği durumu. Kapsam seçeneğinin durumu etkin değil olarak ayarlandıysa, tedarik seçeneği plan türlerinde seçilemez. |
   | **Yüzde** | Yüzde tutarı. Bu alan yalnızca, Kapsam kodu alanında % x maaş seçilmişse etkindir. |
   | **Bölen** | % X maaş kapsam kodunu seçtiğinizde hesaplamada kullanılacak bölen. |
   | **Minimum yüzde** | Yüzde kapsam kodunu seçtiğinizde minimum yüzde. |
   | **Maksimum yüzde** | Yüzde kapsam kodunu seçtiğinizde maksimum yüzde. |

4. **Kişisel ilgili kişi uygunluğu seçenekleri** altında, her kapsam seçeneğine uygun özel ilgili kişiler uygunluk seçeneğini ekleyin.

5. **Self servis** altında, aşağıdaki alanların değerleri belirtin:

   | Alan | Tanım |
   | --- | --- |
   | **Personel katkı tutarına izin ver** | Sosyal haklar seçildiğinde, çalışanların, kazançlar self servis durumunda katkı tutarını değiştirmesine izin verip vermeyeceğini belirtir. Bu onay kutusunu seçerseniz, sistem, sosyal haklar self servis üzerine girdiği katkı tutarını temel alarak, kazanç planı parametrelerini hesaplar. |
   | **Personel karşılama tutarına izin ver** | Sosyal haklar seçildiğinde, çalışanların, kazançlar self servis durumunda kapsam tutarını değiştirmesine izin verip vermeyeceğini belirtir. Bu onay kutusunu seçerseniz, sistem, personel self servis üzerine girdiği kapsam tutarını temel alarak, kazanç planı parametrelerini hesaplar. |

6. **Kaydet**'i seçin. 

---
title: Departmanlar oluşturma ve bunları departman hiyerarşisine dahil etme
description: Bir bölüm bir kuruluşun bir kategori veya işlevsel alanını temsil eden işletme bir birimdir. Departman satış, muhasebe veya İnsan kaynakları gibi kuruluşun belirli bir alanından sorumludur. İşlevsel alanlara bildirmek için bölümleri kullanabilirsiniz. Departmanların kâr ve zarar sorumluluğu olabilir.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HierarchyDesigner, OMOperatingUnit
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: 7b6308c54d237d0d7558fc1f94647f7ca1ab82a1
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/19/2019
ms.locfileid: "858157"
---
# <a name="create-departments-and-include-them-in-the-department-hierarchy"></a>Departmanlar oluşturma ve bunları departman hiyerarşisine dahil etme

[!include [banner](includes/banner.md)]

Bir bölüm bir kuruluşun bir kategori veya işlevsel alanını temsil eden işletme bir birimdir. Departman satış, muhasebe veya İnsan kaynakları gibi kuruluşun belirli bir alanından sorumludur. İşlevsel alanlara bildirmek için bölümleri kullanabilirsiniz. Departmanların kâr ve zarar sorumluluğu olabilir.

Bir departman maliyet merkezleri grubu da içerebilir. Departmanlar için pozisyonlar atanabilir. Bir bölüm oluşturmak için **İnsan Kaynakları** &gt; **Departmanlar** &gt; **Departmanlar** üzerine tıklayın. Aşağıdaki tabloda, kullanılabilecek alanlar açıklanmıştır.

| Alan               | Açıklama                                                                                                                                                                                                       |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dosya Adı                | Departman için bir ad girin.                                                                                                                                                                                  |
| Departman numarası   | **Numara serileri** sayfasında **kuruluş numarası**'na bir numara serisi kodu atadıysanız varsayılan değer otomatik olarak oluşturulabilir.                                                 |
| Arama adı         | Departman için aramada kullanılabilecek bir ad veya kısa ad girin.                                                                                                                                            |
| Not                | Buraya ek bilgi girin                                                                                                                                                                            |
| Hiyerarşide        | Seçili bir onay kutusu, departman hiyerarşisine bir departman dahil edildiğini gösterir. Bir bölümü bölüm hiyerarşisine ekleme hakkında daha fazla bilgi için bu makalenin ilerisindeki bilgilere bakın. |
| DUNS numarası         | DUNS Veri Evrensel Sayı Sistemi anlamına gelir. Bu, Dun & Bradstreet tarafından verilen bir dokuz basamaklı bir sayıdır.                                                                                                     |
| Yönetici             | Departmanı yöneten kişiyi girin.                                                                                                                                                                    |
| Adresler           | Departman için adres bilgilerini ekleyin. Örneğin, departmanın bulunduğunu bina için posta adresini ekleyin.                                                                          |
| İletişim bilgileri | Departman için ilgili kişi verilerini ekleyin. Örneğin, departmanda hizmet masası için bir telefon numarası ekleyin.                                                                                           |

Bölüm hiyerarşisine bir bölüm eklemek için aşağıdaki adımları izleyin.

1.  **İnsan Kaynakları** &gt; **Departmanlar** &gt; **Departman hiyerarşisi**'ni tıklatın.
2.  **Düzenle**'yi tıklatın ve departmanın altında olması gereken kuruluş seçin.
3.  **Ekle**'yi seçin ve listede **Departman**'ı seçin.
4.  Görüntülenen departman listesinde hiyerarşiye eklemek için departmanı seçin.
5.  Değişikliklerinizi kaydedin. Hiyerarşi taslak sürümünü oluşturulduğuna dair bir ileti alırsınız.
6.  Hazır olduğunuzda, hiyerarşisi tasarımcısı içerisinde **Yayımla**'yı tıklatın. Hiyerarşinin ne zaman yayımlanacağını belirtecek bir geçerlilik tarihi girebilirsiniz. Örneğin, bir sonraki takvim yılı başına yeni bir departman eklemek için yürürlük tarihini yeni takvim yılının 1 Ocak'ı olarak ayarlayın. Hiyerarşi değişiklikleri o tarihte geçerlilik kazanır.

## <a name="steps-for-creating-a-department"></a>Bir departman oluşturma adımları
Yeni bir departman oluşturmaya ilişkin adım adım yordam için [Yeni departmanlar tanımlama](../fin-and-ops/hr/tasks/define-new-departments.md) konusuna başvurun. 

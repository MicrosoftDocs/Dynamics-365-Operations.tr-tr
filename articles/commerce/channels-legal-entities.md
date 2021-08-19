---
title: Tüzel kişilik oluşturma
description: Bu konuda, Microsoft Dynamics 365 Commerce'te kanallar oluşturulmadan önce oluşturulup yapılandırılması gereken tüzel kişiliklerin nasıl oluşturulacağı açıklanmaktadır.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: bc5f097a7f941dfa05f4011d9be5caffbb7f01b5f6e67cd7535ef3d1b13f59fe
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6740443"
---
# <a name="create-legal-entities"></a>Tüzel kişilik oluşturma

[!include [banner](includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce'te kanallar oluşturulmadan önce oluşturulup yapılandırılması gereken tüzel kişiliklerin nasıl oluşturulacağı açıklanmaktadır.

Tüzel kişilik, kayıtlı veya asal bir yapıya sahip olan bir organizasyondur. Tüzel kişilikler yasal sözleşmelere girebilir ve performanslarını raporlayacak bildirimler hazırlamaları gerekir.

Bir şirket, tüzel kişilik türüdür. Şu anda oluşturabileceğiniz tek tüzel kişilik türü şirketlerdir ve her bir tüzel kişilik, bir şirket kimliği ile ilişkilendirilir. Bu ilişkilendirmenin nedeni programdaki bazı işlevsel alanların şirket kimliğini veya *DataAreaId*'yi kendi veri modellerinde kullanmasıdır. Bu işlevsel alanlarda, şirketler veri güvenliği için bir sınır olarak kullanılır. Kullanıcılar, yalnızca oturum açmış oldukları şirketin verilerine erişebilir. 

Bir kanal oluştururken, o kanalın ait olduğu tüzel kişiliği belirtmeniz gerekir.

## <a name="create-a-new-legal-entity"></a>Yeni bir tüzel kişilik oluşturma

Dynamics 365 Commerce'te yeni bir tüzel kişilik oluşturmak için bu adımları izleyin.

1. Gezinti bölmesinde, **Modüller \> Headquarters kurulumu \> Tüzel kişilikler**'e gidin.
1. Eylem bölmesinde **Yeni**'yi seçin. **Yeni tüzel kişilik** bölmesi sağda görünür.
1. **Ad** alanına bir değer girin.
1. **Şirket** alanına bir değer girin.
1. **Ülke/bölge** alanına bir değer girin veya buradan bir değer seçin.
1. **Tamam**'ı seçin. 

   ![Tüzel kişilik oluşturma.](media/legal-entities.png)

1. **Genel** bölümünde, tüzel kişilik hakkında aşağıdaki genel bilgileri girin: 
   1. Arama adı gerekiyorsa bir arama adı girin. Arama adı, bu tüzel kişilik için arama yapılmasında kullanılabilecek alternatif bir addır. 
   1. Bu tüzel kişiliğin bir konsolidasyon şirketi olarak kullanılıp kullanılmadığını seçin.
   1. Bu tüzel kişiliğin bir eliminasyon şirketi olarak kullanılıp kullanılmadığını seçin. 
   1. Kişilik için **varsayılan dili** seçin. 
   1. Kişilik için **saat dilimini** seçin.
1. **Adresler** bölümünde, sokak adı ve numarası, posta kodu ve şehir gibi adres bilgilerini girmek için **Düzenle**'yi seçin.
1. **İletişim bilgileri** bölümünde e-posta adresleri, URL'ler ve telefon numaraları gibi iletişim yöntemleri hakkında bilgi girin.
1. **Yasal raporlama** bölümünde, yasal raporlama için kullanılan kayıt numaralarını girin.
1. **Kayıt numaraları** bölümünde, tüzel kişilik tarafından istenen bilgileri girin.
1. **Banka hesabı bilgileri** bölümünde, tüzel kişilik için banka hesaplarını ve rota numaralarını girin.
1. **Dış Ticaret ve lojistik** bölümünde, tüzel kişilik sevkiyat bilgilerini girin.
1. **Numara serileri** bölümünde, tüzel kişilikle ilişkili numara serilerini görüntüleyebilirsiniz. Bu, başlangıçta boş olacaktır.
1. **Pano resmi** bölümünde, tüzel kişilikle ilişkili logoyu ve pano görüntüsünü görüntüleyin veya değiştirin.
1. **Vergi kaydı** bölümünde, vergi kurumlarına bildirilirken kullanılacak kayıt numaralarını girin.
1. **Vergi 1099** bölümüne tüzel kişilik için 1099 bilgilerini girin.
1. **Vergi bilgileri** bölümünde, tüzel kişilik için vergi bilgilerini girin.
1. **Kaydet**'i seçin.

Aşağıdaki resimde örnek bir tüzel kişiliğin ayrıntıları gösteriliyor.

![Tüzel kişilik genel bölümü.](media/legal-entities-general.png)
   
## <a name="additional-resources"></a>Ek kaynaklar

[Kuruluşlar ve kuruluş hiyerarşilerine genel bakış](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Kuruluş hiyerarşinizi planlama](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[Kuruluş hiyerarşileri](channels-org-hierarchies.md)

[Kanallara genel bakış](channels-overview.md)

[Kanal kurulum önkoşulları](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

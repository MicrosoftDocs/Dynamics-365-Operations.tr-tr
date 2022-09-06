---
title: Hediye kartları için şirketler arası veri paylaşımı
description: Bu makalede, veri alanlarında hediye kartı verilerini eşitlemek için Microsoft Dynamics 365 Commerce'ın açıklanır Dynamics 365 Finance veri paylaşım işlevini kullanmak üzere nasıl yapılandırılabileceği açıklanmaktadır.
author: BrianShook
ms.date: 08/26/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-06-20
ms.openlocfilehash: b56890b546c3cd74b75cf447e62495733ea8d288
ms.sourcegitcommit: 09d4805aea6d148de47c8ca38d8244bbce9786ce
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/31/2022
ms.locfileid: "9387077"
---
# <a name="cross-company-data-sharing-for-gift-cards"></a>Hediye kartları için şirketler arası veri paylaşımı

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce'ı hediye kartı verilerini eşitlemek için Dynamics 365 Finance veri paylaşım işlevini kullanmak üzere nasıl yapılandıracağınız açıklanmaktadır. Veri kaydı paylaşma işlevi, iki veri alanı arasında verileri şitkerler arasında paylaşmak için kullanılabilir. Bu şekilde, Commerce dahili hediye tablosu verileri iki şirket varlığı arasında paylaşabilir. Dynamics 365 Finance şirketler arası veri paylaşımı hakkında daha fazla bilgi için bkz. [Şirketler arası veri paylaşımı](/dynamics365/fin-ops-core/dev-itpro/sysadmin/cross-company-data-sharing).

## <a name="key-terms"></a>Önemli terimler

| Vade | Açıklama |
|---|---|
| Şirket | Dynamics 365 Finance ortamındaki tüzel kişilik. |
| Hediye kartı | Dynamics 365 Commerce dahili hediye kartı ürünü. |

## <a name="prerequisites"></a>Ön Koşullar

Kullanıcılar, ortamlarını [Şirketler arası veri paylaşımı](/dynamics365/fin-ops-core/dev-itpro/sysadmin/cross-company-data-sharing) bölümünde açıklandığı şekilde veri paylaşımı için yapılandırmalıdır.

Hediye kartı tablosu için yinelenen kayıt paylaşımını (DRS) etkinleştirmek için **RetailGiftCardTable** tablosunda **DataSharingType** alanı **Yinele** olarak ayarlanmalıdır. Daha fazla bilgi için bkz. [Geliştiriciler için şirketler arası veri paylaşımı](/dynamics365/fin-ops-core/dev-itpro/sysadmin/drs-srs-dev).

## <a name="configure-cross-company-data-sharing-for-gift-cards"></a>Hediye kartları için şirketler arası veri paylaşımını yapılandırma

Hediye kartları için şirketler arası veri paylaşımını yapılandırmak üzere aşağıdaki adımları izleyin.

1. Commerce Headquarters'da **Sistem yönetimi \> Kurulum \> Şirketler arası veri paylaşımını yapılandır** seçeneğine gidin.
1. Veri paylaşımı kaydı eklemek için Eylem Bölmesinde **Yeni**'yi seçin.
1. **Ad** alanına, veri paylaşım kaydı için bir ad girin (örneğin, **Hediye Kartları**).
1. **Tablolar ve paylaşılacak alanlar** bölümünde **Ekle**'yi seçin.
1. **Yeni tablo paylaş** iletişim kutusunda **Tablo adı** alanına **RETAILGIFTCARDTABLE** (perakende hediye kartları için tablo) girin. **Tablo etiketi** alanı otomatik olarak **Hediye kartı tablosu** olarak ayarlanmalıdır.
1. **Şirket başına verileri kaydet**, **Benzersiz dizine sahip** ve **Henüz paylaşılmadı** onay kutularının tümünün seçili olduğundan emin olun. Bu onay kutularının seçilmesi, veri paylaşımı işleviyle ilgili doğrulamaları tetikler.
1. **Tablo ekle**'yi seçin. **Hediye kartı tablosu (RetailGiftCardTable)** kaydı artık **Paylaşılacak tablolar ve alanlar** altında görünmelidir. Paylaşım için tabloyla otomatik olarak ilişkilendirilen tüm tablo alanlarını görüntülemek için şapka işaretini (^) seçin.
1. **Bu tablolarda kayıtları paylaşan şirketler**  bölümünde verileri paylaşmak için bir şirket eklemek üzere **Ekle**'yi seçin.
1. **Şirket** altındaki satırda açılan listeden bir şirket seçin.
1. **Ad** alanına şirket adını girin.
1. Daha fazla şirket satırı eklemek için 8. ile 10. adımlar arasındaki işlemleri tekrarlayın.
1. Şirket satırlarını eklemeyi bitirdiğinizde Eylem Bölmesinde **Etkinleştir**'i seçin.
1. Şu ifadeyi içeçren bir uyarı iletisi alırsınız: "Bu eylemi iş saatleri dışında gerçekleştirmeniz önerilir. Tüm eşzamanlı işlem operasyonları ilkedeki tablolar için başarısız olacak. Devam etmek istiyor musunuz?" Kabul etmek için **Evet**'i seçin.
1. "Var olan tüm verileri şimdi tüm paylaşılan şirketler arasında kopyalamak istiyor musunuz?" ifadesini içeren bir uyarı iletisi alırsınız Kabul etmek için **Evet**'i seçin.

Her iki iletiyi de kabul ettikten sonra tablolar yapılandırılan şirketler arasında veri kopyalamaya başlar. Bir şirket hediye kartıyla ilgili olarak gerçekleşen bakiyeler diğer şirket tarafından görülebilir duruma gelir.

## <a name="additional-resources"></a>Ek kaynaklar

[Ödemeler ile ilgili SSS](payments-retail.md)

[Ödeme yapma modülü](../add-checkout-module.md)

[Ödeme modülü](../payment-module.md)

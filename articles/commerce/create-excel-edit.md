---
title: Perakende hareketlerini düzenlemek için bir Excel çalışma kitabı oluşturma
description: Bu makalede, Microsoft Dynamics 365 Commerce'te perakende hareketlerini düzenleyebilmek için nasıl Excel çalışma kitabı oluşturabileceğiniz açıklanmaktadır.
author: josaw1
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.industry: Retail
ms.openlocfilehash: 93e0053c38c9595cab59947e4b65b0b4aa966380
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270223"
---
# <a name="create-an-excel-workbook-to-edit-retail-transactions"></a>Perakende hareketlerini düzenlemek için bir Excel çalışma kitabı oluşturma

[!include [banner](../includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce'te perakende hareketlerini düzenleyebilmek için nasıl Excel çalışma kitabı oluşturabileceğiniz açıklanmaktadır.

## <a name="overview"></a>Genel bakış

Müşterilerin sistemin farklı bölümlerinden erişebilecekleri ve perakende hareketlerini düzenleyip denetlemek için kullanabilecekleri önceden tanımlanmış bir Excel şablonu bulunur. Ancak müşteriler bu amaçla özel bir Excel çalışma kitabı da oluşturabilirler.

## <a name="create-and-configure-an-excel-workbook"></a>Excel çalışma kitabı oluşturma ve yapılandırma

Perakende hareketlerini düzenleyebileceğiniz bir Excel çalışma kitabı oluşturmak ve yapılandırmak için aşağıdaki adımları izleyin.

1. Excel'i açın ve boş bir çalışma kitabı oluşturun.
1. **Ekle** sekmesinde, **Eklentilerim**'i seçin.
1. Sağ bölmede, **Sunucu bilgilerini ekle** bağlantısını seçin.
1. Sunucu URL'sini girin ve ardından **Tamam**'ı seçin.
1. "Uygulama kaydı bulunamadı" hata iletisini alırsanız sorunu çözmek için şu adımları izleyin:

    1. Commerce uygulamasında, **Sistem yönetimi \> Ayar \> Office uygulaması parametreleri** bölümüne gidin.
    1. **Uygulama parametreleri** hızlı sekmesinde, **Uygulama parametrelerini başlat**'ı seçin.
    1. Onay iletisi kutusunda **Tamam**'ı seçin.
    1. **Kayıtlı uygulamalar** hızlı sekmesinde, **Uygulama kaydını başlat**'ı seçin.
    1. Gerekirse önceki üç adımı tekrarlayın.

1. **Tasarım**'ı ve ardından **Tablo ekle**'yi seçin.
1. Değiştirilmesi gereken verilere bağlı olarak, düzenlenmek üzere Excel çalışma kitabına eklenmesi gereken varlıkları seçin. Referans olarak aşağıdaki tabloyu kullanın.

    | Hareket türü | Kullanılacak veri varlıkları |
    |------------------|----------------------|
    | Peşin hareketler, Çevrimiçi siparişler, Zaman uyumsuz müşteri siparişleri, Zaman uyumsuz müşteri teklifleri | Hareket (denetlenebilir), Satış hareketi (denetlenebilir), Ödeme hareketleri (denetlenebilir), Vergi hareketleri (denetlenebilir), İskonto hareketleri (denetlenebilir), Masraf hareketleri (denetlenebilir) |
    | Bankaya para nakli | Hareket (denetlenebilir), Bankaya nakledilen ödeme hareketleri (denetlenebilir) |
    | Kasaya para nakli | Hareket (denetlenebilir), Kasa ödemesi hareketleri (denetlenebilir) |
    | Kasa sayımı | Hareket (denetlenebilir), Kasa sayımı hareketleri (denetlenebilir) |
    | Gelir, Gider | Hareket (denetlenebilir), Gelir/Gider hareketleri (denetlenebilir), Ödeme hareketleri (denetlenebilir) |
    | Başlangıç tutarını beyan etme, Ödeme kaldırma, Kasa devri girişi, Para üstü ödeme, Fatura ödeme, Müşteri havalesi | Hareket (denetlenebilir), Ödeme hareketleri (denetlenebilir) |

    > [!NOTE]
    > Her Excel çalışma kitabına yalnızca bir veri varlığı eklemeniz önemlidir. Ek olarak, bir anahtar simgesiyle işaretlenmiş tüm alanlar ilgili çalışma kitabına eklenmelidir.

1. Çalışma kitabı yapılandırıldıktan sonra gerekli filtreleri uygulayın. Dosyadaki tüm çalışma sayfalarına aynı filtreleri uyguladığınızdan emin olun. Excel dosyasına çok büyük miktarlarda veri yüklemekten kaçının. Aksi takdirde performans etkilenebilir, Excel ve sisteminiz yavaşlayabilir. Dosyanızda her zaman "Şirket" ile "Ekstre Numarası" veya "Hareket Numarası" filtrelerini kullanmanızı öneririz.
1. Filtreler yapılandırıldıktan sonra verileri yüklemek için **Yenile**'yi seçin.
1. Gerekli verileri düzenleyin ve ardından yayımlayın. **Yayımla** düğmesi kullanılamıyorsa bazı önemli alanlar Excel çalışma kitabına eklenmemiş olabilir.

## <a name="additional-resources"></a>Ek kaynaklar

[Peşin ve nakit yönetimi hareketlerini düzenleme ve denetleme](edit-cash-trans.md)

[Çevrimiçi siparişi ve zaman uyumsuz müşteri siparişi hareketlerini düzenleme ve denetleme](edit-order-trans.md)

[Perakende hareketlerinin mali boyutlarını düzenleme](edit-financial-dim.md)

[Perakende hareketlerini düzenlemek için Excel çalışma kitabına alanlar ekleme](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

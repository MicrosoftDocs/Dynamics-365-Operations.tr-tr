---
title: İçeriği başka bir yerel ayara kopyalama
description: Bu makalede, mevcut içeriğin Microsoft Dynamics 365 Commerce site oluşturucuda bulunan bir site içindeki başka bir yerel ayara nasıl kopyalanacağı açıklanır.
author: psimolin
ms.date: 07/06/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: bcfa3c7cb2ea8018422803d85df6b6761b8d1145
ms.sourcegitcommit: d719d0a549aecac231fad0abb42250eab9dd0ded
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/07/2022
ms.locfileid: "9126460"
---
# <a name="copy-content-to-another-locale"></a>İçeriği başka bir yerel ayara kopyalama

[!include[banner](../includes/banner.md)]

Bu makalede, mevcut içeriğin Microsoft Dynamics 365 Commerce site oluşturucuda bulunan bir site içindeki başka bir yerel ayara nasıl kopyalanacağı açıklanır.

Ticaret site oluşturucuda içerik oluşturduğunuzda, her zaman "en-us" gibi bir yerel ayar tanımlayıcısıyla ilişkilendirilir. Bir içerik öğesini düzenleyip daha sonra öğenin yeni bir türevini oluştururken, yerel ayarı değiştirerek aynı e-ticaret sitesindeki farklı bir yerel ayara ayrı ayrı sayfalar ve varlıklar kopyalayabilirsiniz. Bazı durumlarda, vitrininizde tümüyle yeni bir yerel ayar başlattığınızda olduğu gibi, mevcut bir yerel ayarda bulunan tüm içerik öğelerini yeni yerel ayara çoğaltmak da mantıklıdır. Yeni yerel ayar mevcut yerel ayarlardan biriyle aynı temel dile sahipse mevcut yerel ayarı, yerel ayar kopyalama işlemi için kaynak yerel ayar olarak kullanabilirsiniz. (Örneğin "en-us" ve "en-au" yerel ayarlarının ikisi de İngilizce dili kullanır.) Bu şekilde, yeni yerel ayarda içeriği yerelleştirmek için gereken çabayı azaltmaya yardımcı olursunuz.

Aşağıdaki yordamlarda, mevcut bir kanala yeni yerel ayarın nasıl ekleneceği, tüm içerik öğelerinin mevcut bir yerel ayardan yeni bir yerel ayara nasıl kopyalanacağı ve yerel ayar kopyalama işleminin durumunu nasıl izleneceği açıklanmaktadır.

## <a name="add-a-new-locale"></a>Yeni bir yerel ayar ekle

Ticaret site oluşturucuda yeni bir yerel ayar oluşturmak için aşağıdaki adımları izleyin.

1. Site oluşturucuda sitenize gidin.
1. Sol gezinti bölmesinde, **Site ayarları**'nı seçin ve sonra **Kanallar**'ı seçin.
1. **Kanal** altında yeni yerel ayarın ekleneceği kanalı seçin.
1. Sağda görünen kanal iletişim kutusunda **Yerel ayar ekle**'yi seçin.
1. **Yerel ayar ekle** iletişim kutusunda, **Desteklenecek yerel ayar** alanında bir yerel ayar seçin.
1. **Etki alanı** değerinin doğru olduğunu onaylayın.
1. **Yol** altında, benzersiz bir URL yolu (örneğin **en-us** veya **english-us**) girin.
1. **Tamam**'ı seçin.
1. Kanal iletişim kutusunu kapatın.
1. **Kanal** altında, yeni yerel ayarın doğru kanalın yanında listelendiğini doğrulayın.
1. **Kaydet ve yayınla** yı seçin.

> [!NOTE]
> Yeni yerel ayarın site oluşturucuda yapılandırılabilmesi için önce Commerce headquarters'taki ilişkili çevrimiçi mağaza kanalına eklenmesi gerekir.

## <a name="copy-all-content-items-to-a-new-locale"></a>Tüm içerik öğelerini yeni bir yerel ayara kopyalama

Tüm içerik öğelerini, ticaret site oluşturucuda yeni bir yerel ayara kopyalamak için aşağıdaki adımları izleyin.

1. Site oluşturucuda sitenize gidin.
1. Sol gezinti bölmesinde, **Site ayarları**'nı seçin ve sonra **Kanallar**'ı seçin.
1. Komut çubuğunda, **Yerel ayar kopyası oluştur**'u seçin.
1. Sağ tarafta görünen **Yerel ayar kopyası oluştur** iletişim kutusundaki **Kaynak site** altında doğru sitenin seçili olduğunu doğrulayın.
1. **Kaynak kanal** alanında, kaynak kanalı seçin.
1. **Hedef kanal** alanında, ayni kaynak kanalı seçin.
1. **Kaynak yerel ayar** alanında, kaynak yerel ayarı seçin.
1. **Hedef yerel ayar** alanında, yeni yerel ayarı seçin.
1. **Yerel ayar kopyala**'yı seçin. Bir bildirim, yerel ayar kopyalama işleminin başladığını onaylar.

> [!NOTE]
> Ayrıca, içeriği farklı kanallar arasında kopyalayabilirsiniz.

## <a name="monitor-the-status-of-the-locale-copy"></a>Yerel ayar kopyasının durumunu izleme

Bir yerel kopyalama işleminin durumunu izlemek için aşağıdaki adımları izleyin.

1. Site oluşturucuda sitenize gidin.
1. Sol gezinti bölmesinde, **Site ayarları**'nı seçin ve sonra **İşler**'i seçin.
1. **Mevcut işler** altında, izlenecek işi seçin. İş detayları, sağda görünen iletişim kutusunda gösterilir.

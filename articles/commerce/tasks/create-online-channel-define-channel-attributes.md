---
title: Çevrimiçi kanal oluştur ve kanal özniteliklerini tanımla
description: Bu yordam yeni bir çevrimiçi kanal oluşturma ve kuruluş hiyerarşisine ekleme konusunda rehberlik sağlar.
author: jashanno
manager: AnnBe
ms.date: 06/04/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailSPOnlineStoreDetailPage, SysLookupMultiSelectGrid, DimensionLookup, OMHierarchyManager, HierarchyDesigner, OMNodeSelection, HierarchyPublishAndCloseForm
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8e92e28c721692ed92fa931ed899c48678622349
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4964807"
---
# <a name="create-online-channel-and-define-channel-attributes"></a>Çevrimiçi kanal oluştur ve kanal özniteliklerini tanımla

[!include [banner](../includes/banner.md)]

Bu yordam yeni bir çevrimiçi kanal oluşturma ve kuruluş hiyerarşisine ekleme konusunda rehberlik sağlar. Yeni bir çevrimiçi kanal oluşturmadan önce kuruluş hiyerarşisi oluşturmanız gerekir. Bu yordam, USRT demo veri şirketini kullanır.


## <a name="create-a-new-online-channel"></a>Yeni çevrimiçi kanal oluşturma
1. Retail and Commerce > Kanallar > Çevrimiçi mağazalar'a gidin.
2. Yeni'yi tıklatın.
3. İsim alanına bir değer yazın.
4. Ambar alanında bir değer girin veya bir değer seçin.
5. Mağaza saat dilimi alanında bir seçenek seçin.
6. Varsayılan müşteri alanına bir değer girin veya buradan bir değer seçin.
7. Müşteri adres defteri alanına bir değer girin veya buradan bir değer seçin.
8. Ödeme koşulları alanına bir değer girin veya buradan bir değer seçin.
9. Ödeme yöntemi alanında bir değer girin veya bir değer seçin.
10. E-posta bildirim profili alanına bir değer girin veya buradan bir değer seçin.
11. Mali boyutlar bölümünü genişletin.
12. BusinessUnit alanına bir değer girin veya buradan bir değer seçin.
    * Benzer şekilde, diğer tüm varsayılan boyutlar için değeri ayarlayın.  
13. Kaydet'e tıklayın.

## <a name="add-the-online-channel-to-organization-hierarchy"></a>Çevrimiçi kanalı kuruluş hiyerarşisine ekle
1. Sayfayı kapatın.
2. Organizasyon yönetimi > Kuruluşlar > Kuruluş hiyerarşileri öğesine gidin.
3. Listede, istenen kaydı bulun ve seçin.
4. Görüntüle'ye tıklayın.
5. Düzenle öğesine tıklayın.
    * Yeni kanal eklemek istediğiniz herhangi bir hiyerarşi düğümünü seçebilirsiniz.  
6. Ekle'yi tıklatın.
7. Commerce kanalına tıklayın.
8. Tamam'a tıklayın.
9. İletişim kutusunu açmak için Yayımla'ya tıklayın.
10. Yürürlük tarihi alanına bir tarih ve saat girin.
11. Yayımla'ya tıklayın.

## <a name="configure-orders-for-near-real-time-notification"></a>Gerçek zamanlı bildirim yakınlarında siparişleri yapılandırma
1. Retail ve Commerce > Headquarters ayarı > Parametreler > Commerce parametreleri'ne gidin.
2. eCommerce sipariş oluşturma için gerçek zamanlı hizmeti "Evet" olarak ayarla.
3. Değişiklikleri kanal veritabanıyla eşitlemek için 1070 dağıtım planını yürütün. 




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: Çevrimiçi mağazaları konfigüre et
description: Bu makale, bir çevrimiçi mağazayı merkezi olarak yapılandırma ve yönetme hakkında yardımcı olacak konulara bağlantılar sağlar.
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: robinr
ms.search.scope: Operations, Retail
ms.custom: 31541
ms.assetid: 7a25f9b4-a0bb-4e8c-95c0-c0799ec0620d
ms.search.region: Global
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: d353baf67540b64168f29be3506d73e721e73523
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "354380"
---
# <a name="configure-online-stores"></a>Çevrimiçi mağazaları konfigüre et

[!include [banner](../includes/banner.md)]

Bu makale, bir çevrimiçi mağazayı merkezi olarak yapılandırma ve yönetme hakkında yardımcı olacak konulara bağlantılar sağlar.

Aşağıdaki tabloda listelenen konular, Retail bileşenlerini ve istemcideki Retail çevrimiçi mağazayı yapılandırmanıza yardımcı olur.

## <a name="configure-an-online-store"></a>Bir çevrimiçi mağazayı yapılandırma

| Görev                                                | Ayrıntılı                                                                                                                                                                                                                                                                                                                                                   | Konular                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Perakende bileşenlerini yapılandır.                        | Perakende operasyonları için bilgiyi ayarlama ve saklama. Bu bilgiler, mağazalar, vergiler, ürünler, hediye kartları, promosyonlar ve indirimleri içerir.                                                                                                                                                                                                          | [Perakende'yi kurmak ve korumak](https://technet.microsoft.com/en-us/library/hh597201.aspx) (Microsoft Dynamics AX 2012 için TechNet içeriği)                                                                                                                                                                                                                                                                                          |
| Bir perakende kanlı gezinme hiyerarşisi oluştur.    | Çevrimiçi bir mağazayla sunduğunuz ürünler için bir kategori yapısı ayarlamak için perakende kanalı gezinti kategori hiyerarşisi oluşturun. Kategori hiyerarşisini tanımlar ve ürünler, ürün öznitelik grupları ve öznitelik değerlerini kategorilere atayabilirsiniz. Daha sonra çevrimiçi bir mağazaya kategori hiyerarşisi atarsınız.                            | [Bir perakende hiyerarşisini ayarlama](https://technet.microsoft.com/en-us/library/hh580593.aspx) (AX 2012 için TechNet içeriği) [Öznitelikleri ve öznitelik türlerini ayarlama](https://technet.microsoft.com/en-us/library/hh227548.aspx) (AX 2012 için TechNet içeriği) [Perakende öznitelik gruplarını ayarlamak](https://technet.microsoft.com/en-us/library/jj728713.aspx) (AX 2012 için TechNet içeriği) |
| Çevrimiçi mağazayı kuruluş hiyerarşisine ekleyin. | Oluşturmuş olduğunuz çevrimiçi mağazaya ürün sınıflarını atayabilmeden veya siparişleri yerine getirebilmeden veya bu çevrimiçi mağazadan bilgileri içeren raporlar oluşturabilmeden önce, mağazayı bir ya da birden fazla kuruluş hiyerarşisine atamanız gerekir. En azından, çevrimiçi mağazayı ürün sınıfları içeren bir kuruluş hiyerarşisine atamanız gerekir. | [Bir çevrimiçi mağaza kurmak](https://technet.microsoft.com/en-us/library/jj682095.aspx) (AX 2012 için TechNet içeriği)                                                                                                                                                                                                                                                                                                     |
| Çevrimiçi mağazaya teslimat şekli ekle.          | Çevrimiçi mağazanın sunduğu teslimat yöntemlerini seçin.                                                                                                                                                                                                                                                                                                 | [Bir çevrimiçi mağaza kurmak](https://technet.microsoft.com/en-us/library/jj682095.aspx) (Microsoft AX 2012 için TechNet içeriği)                                                                                                                                                                                                                                                                                                     |
| Öznitelikleri eşle ve meta veri ekle.                   | Her kategori veya kanal ürününün Microsoft SharePoint sitesi çevrimiçi mağazasındaki özniteliklerin nasıl davranacağını belirten seçenekleri işaretleyin.                                                                                                                                                                                              | [Bir çevrimiçi mağaza kurmak](https://technet.microsoft.com/en-us/library/jj682095.aspx) (AX 2012 için TechNet içeriği)                                                                                                                                                                                                                                                                                                     |

## <a name="configure-online-store-products"></a>Çevrimiçi mağaza ürünlerini yapılandır

| Görev                                 | Ayrıntılı                                                                                                                                           | Konular                                                                                                                                                                                                                                                                            |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Çevrimiçi mağazaya ürün çeşidi ekle. | Bir çevrimiçi mağazada sunduğunuz ürünleri içeren sınıfları ekleyin.                                                                  | [Bir çevrimiçi mağaza kurmak](https://technet.microsoft.com/en-us/library/jj682095.aspx) (AX 2012 için TechNet içeriği)                                                                                                                                              |
| Katalogları yönet.                     | Mağazalarınızda sunmak istediğiniz ürünleri belirlemek için ürün kataloglarını kullanın.                                                              | [Anahtar görevler: Perakende ürün katalogları oluşturmak](https://technet.microsoft.com/en-us/library/jj728712.aspx) (AX 2012 için TechNet içeriği)                                                                                                                           |
| Fiyatları yönetin.                       | Fiyatlar ve indirimler, kanallar, kataloglar, bağlantılar ve bağlılık programları arasında merkezi bağlantı olan fiyat gruplarını ayarlayın ve kullanın. | [Fiyat grupları kullanarak fiyatları ayarlamak](https://technet.microsoft.com/en-us/library/hh597169.aspx) (AX  2012 için TechNet içeriği) [Vergileri ayarlama](https://technet.microsoft.com/en-us/library/hh580571.aspx) (AX 2012 için TechNet içeriği) |
| İskontoları yönetmek.                    | Dört tür indirim ve fiyat ayarlamalarını ayarlamak ve yönetmek.                                                                                  | [Fiyat ayarlamalarını ve iskontoları kurmak ve korumak](https://technet.microsoft.com/en-us/library/hh597114.aspx) (AX 2012 için TechNet içeriği)                                                                                                                          |
| Sevkiyat masraflarını yönetmek.             | Çevrimiçi mağazaya özel kargo ücretlerini ayarlayın ve yönetin.                                                                     | [Çevrimiçi mağazalar için kargo masraflarını ayarlamak](https://technet.microsoft.com/en-us/library/jj728714.aspx) (AX 2012 için TechNet içeriği)                                                                                                                           |
| Teslimat şekillerini yönet.            | Çevrimiçi mağazanın sunduğu teslimat modlarını yönetin.                                                                                        | [Teslimat modlarını ayarlamak](https://technet.microsoft.com/en-us/library/jj728719.aspx) (AX 2012 için TechNet içeriği)                                                                                                                                            |

## <a name="set-up-data-exchange-between-microsoft-dynamics-365-for-retail-and-the-online-store"></a>Microsoft Dynamics 365 for Retail ve çevrimiçi mağaza arasındaki veri değişimini ayarlayın

| Görev                                 | Ayrıntılı                                                                                                                               | Konular                                                                                                                                                                                                                                                                                  |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kanal tümleştirme profillerini ayarlayın. | Profiller, Perakende bileşenlerinin birbirleriyle iletişim kurabilmesini sağlar. Veri değişimi ayarlarını yapılandırmadan önce profiller ayarlayın. | [Gerçek zamanlı hizmet profili kurmak](https://technet.microsoft.com/en-us/library/hh580631.aspx) (AX 2012 için TechNet içeriği) [Bir kanal profili kurmak](https://technet.microsoft.com/en-us/library/jj677402.aspx) (AX 2012 için TechNet içeriği) |






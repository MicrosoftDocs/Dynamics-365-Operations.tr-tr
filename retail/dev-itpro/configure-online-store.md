---
title: "Bir çevrimiçi mağazayı yapılandırma"
description: "Bu makale, Microsoft Dynamics 365 for Operations içerisinden bir çevrimiçi mağazayı merkezi olarak yapılandırma ve yönetme hakkında konulara bağlantılar sağlayacaktır."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Retail
ms.custom: 31541
ms.assetid: 7a25f9b4-a0bb-4e8c-95c0-c0799ec0620d
ms.search.region: Global
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 29938d962db42a521dd8dc03b8e45e0e34410e4d
ms.openlocfilehash: 4da710b57d03621fdf9abbf5a9598859e1e9aafd
ms.lasthandoff: 03/31/2017


---

# <a name="configure-an-online-store"></a>Bir çevrimiçi mağazayı yapılandırma

[!include[banner](../includes/banner.md)]


Bu makale, Microsoft Dynamics 365 for Operations içerisinden bir çevrimiçi mağazayı merkezi olarak yapılandırma ve yönetme hakkında konulara bağlantılar sağlayacaktır.

Aşağıdaki tabloda listelenen konular, Dynamics 365 for Operations - Perakende bileşenlerini ve Perakende çevrimiçi mağazasını Dynamics 365 for Operations istemcisinden yapılandırmanıza yardımcı olacaktır.

## <a name="configure-an-online-store"></a>Bir çevrimiçi mağazayı yapılandırma
| Görev                                                | Ayrıntılı                                                                                                                                                                                                                                                                                                                                                   | Konular                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Perakende bileşenlerini yapılandır.                        | Perakende operasyonları için bilgiyi ayarlama ve saklama. Bu bilgiler, mağazalar, vergiler, ürünler, hediye kartları, promosyonlar ve indirimleri içerir.                                                                                                                                                                                                          | [Perakende'yi kurmak ve korumak](https://technet.microsoft.com/en-us/library/hh597201.aspx) (Microsoft Dynamics AX 2012 için TechNet içeriği)                                                                                                                                                                                                                                                                                          |
| Bir perakende kanlı gezinme hiyerarşisi oluştur.    | Çevrimiçi bir mağazayla sunduğunuz ürünler için bir kategori yapısı ayarlamak için perakende kanalı gezinti kategori hiyerarşisi oluşturun. Kategori hiyerarşisini tanımlar ve ürünler, ürün öznitelik grupları ve öznitelik değerlerini kategorilere atayabilirsiniz. Daha sonra çevrimiçi bir mağazaya kategori hiyerarşisi atarsınız.                            | [Bir perakende hiyerarşisini ayarlama](https://technet.microsoft.com/en-us/library/hh580593.aspx) (Microsoft Dynamics AX 2012 için TechNet içeriği) [Öznitelikleri ve öznitelik türlerini ayarlama](https://technet.microsoft.com/en-us/library/hh227548.aspx) (Microsoft Dynamics AX 2012 için TechNet içeriği) [Perakende öznitelik gruplarını ayarlamak](https://technet.microsoft.com/en-us/library/jj728713.aspx) (Microsoft Dynamics AX 2012 için TechNet içeriği) |
| Çevrimiçi mağazayı kuruluş hiyerarşisine ekleyin. | Oluşturmuş olduğunuz çevrimiçi mağazaya ürün sınıflarını atayabilmeden veya siparişleri yerine getirebilmeden veya bu çevrimiçi mağazadan bilgileri içeren raporlar oluşturabilmeden önce, mağazayı bir ya da birden fazla kuruluş hiyerarşisine atamanız gerekir. En azından, çevrimiçi mağazayı ürün sınıfları içeren bir kuruluş hiyerarşisine atamanız gerekir. | [Bir çevrimiçi mağaza kurmak](https://technet.microsoft.com/en-us/library/jj682095.aspx) (Microsoft Dynamics AX 2012 için TechNet içeriği)                                                                                                                                                                                                                                                                                                     |
| Çevrimiçi mağazaya teslimat şekli ekle.          | Çevrimiçi mağazanın sunduğu teslimat yöntemlerini seçin.                                                                                                                                                                                                                                                                                                 | [Bir çevrimiçi mağaza kurmak](https://technet.microsoft.com/en-us/library/jj682095.aspx) (Microsoft Dynamics AX 2012 için TechNet içeriği)                                                                                                                                                                                                                                                                                                     |
| Öznitelikleri eşle ve meta veri ekle.                   | Her kategori veya kanal ürününün Microsoft SharePoint sitesi çevrimiçi mağazasındaki özniteliklerin nasıl davranacağını belirten seçenekleri işaretleyin.                                                                                                                                                                                              | [Bir çevrimiçi mağaza kurmak](https://technet.microsoft.com/en-us/library/jj682095.aspx) (Microsoft Dynamics AX 2012 için TechNet içeriği)                                                                                                                                                                                                                                                                                                     |

## <a name="configure-online-store-products"></a>Çevrimiçi mağaza ürünlerini yapılandır
| Görev                                 | Ayrıntılı                                                                                                                                           | Konular                                                                                                                                                                                                                                                                            |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Çevrimiçi mağazaya ürün çeşidi ekle. | Bir çevrimiçi mağazada sunduğunuz ürünleri içeren sınıfları ekleyin.                                                                  | [Bir çevrimiçi mağaza kurmak](https://technet.microsoft.com/en-us/library/jj682095.aspx) (Microsoft Dynamics AX 2012 için TechNet içeriği)                                                                                                                                              |
| Katalogları yönet.                     | Mağazalarınızda sunmak istediğiniz ürünleri belirlemek için ürün kataloglarını kullanın.                                                              | [Anahtar görevler: Perakende ürün katalogları oluşturmak](https://technet.microsoft.com/en-us/library/jj728712.aspx) (Microsoft Dynamics AX 2012 için TechNet içeriği)                                                                                                                           |
| Fiyatları yönetin.                       | Fiyatlar ve indirimler, kanallar, kataloglar, bağlantılar ve bağlılık programları arasında merkezi bağlantı olan fiyat gruplarını ayarlayın ve kullanın. | [Fiyat grupları kullanarak fiyatları ayarlamak](https://technet.microsoft.com/en-us/library/hh597169.aspx) (Microsoft Dynamics AX 2012 için TechNet içeriği) [Vergileri ayarlama](https://technet.microsoft.com/en-us/library/hh580571.aspx) (Microsoft Dynamics AX 2012 için TechNet içeriği) |
| İskontoları yönetmek.                    | Dört tür indirim ve fiyat ayarlamalarını ayarlamak ve yönetmek.                                                                                  | [Fiyat ayarlamalarını ve iskontoları kurmak ve korumak](https://technet.microsoft.com/en-us/library/hh597114.aspx) (Microsoft Dynamics AX 2012 için TechNet içeriği)                                                                                                                          |
| Sevkiyat masraflarını yönetmek.             | Çevrimiçi mağazaya özel kargo ücretlerini ayarlayın ve yönetin.                                                                     | [Çevrimiçi mağazalar için kargo masraflarını ayarlamak](https://technet.microsoft.com/en-us/library/jj728714.aspx) (Microsoft Dynamics AX 2012 için TechNet içeriği)                                                                                                                           |
| Teslimat şekillerini yönet.            | Çevrimiçi mağazanın sunduğu teslimat modlarını yönetin.                                                                                        | [Teslimat modlarını ayarlamak](https://technet.microsoft.com/en-us/library/jj728719.aspx) (Microsoft Dynamics AX 2012 için TechNet içeriği)                                                                                                                                            |

## <a name="set-up-data-exchange-between-dynamics-365-for-operations-and-the-online-store"></a>Dynamics 365 for Operations ve çevrimiçi mağaza arasındaki veri değişimini ayarlayın
| Görev                                 | Ayrıntılı                                                                                                                               | Konular                                                                                                                                                                                                                                                                                  |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kanal tümleştirme profillerini ayarlayın. | Profiller, Perakende bileşenlerinin birbirleriyle iletişim kurabilmesini sağlar. Veri değişimi ayarlarını yapılandırmadan önce profiller ayarlayın. | [Gerçek zamanlı hizmet profili kurmak](https://technet.microsoft.com/en-us/library/hh580631.aspx) (Microsoft Dynamics AX 2012 için TechNet içeriği) [Bir kanal profili kurmak](https://technet.microsoft.com/en-us/library/jj677402.aspx) (Microsoft Dynamics AX 2012 için TechNet içeriği) |

 





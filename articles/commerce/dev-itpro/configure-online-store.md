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
ms.reviewer: rhaertle
ms.custom: 31541
ms.assetid: 7a25f9b4-a0bb-4e8c-95c0-c0799ec0620d
ms.search.region: Global
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: cf7adf76cb547ffbf516ce475380ddafaca1dfc6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5215474"
---
# <a name="configure-online-stores"></a>Çevrimiçi mağazaları konfigüre et

[!include [banner](../includes/banner.md)]

Bu makale, bir çevrimiçi mağazayı merkezi olarak yapılandırma ve yönetme hakkında yardımcı olacak konulara bağlantılar sağlar.

Aşağıdaki tabloda listelenen konular, Commerce bileşenlerini ve istemcideki çevrimiçi mağazayı yapılandırmanıza yardımcı olur.

## <a name="configure-an-online-store"></a>Bir çevrimiçi mağazayı yapılandırma

| Görev                                                | Ayrıntılı                                                                                                                                                                                                                                                                                                                                                   | Konular                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bileşenleri yapılandırın.                        | Commerce operasyonları için bilgileri ayarlayın ve saklayın. Bu bilgiler, mağazalar, vergiler, ürünler, hediye kartları, promosyonlar ve indirimleri içerir.                                                                                                                                                                                                          | [Perakende'yi kurmak ve korumak](https://technet.microsoft.com/library/hh597201.aspx) (Microsoft Dynamics AX 2012 için TechNet içeriği)                                                                                                                                                                                                                                                                                          |
| Bir kanal gezinme hiyerarşisi yapılandırın.    | Çevrimiçi bir mağazayla sunduğunuz ürünler için bir kategori yapısı ayarlamak için kanal gezinti kategori hiyerarşisi oluşturun. Kategori hiyerarşisini tanımlar ve ürünler, ürün öznitelik grupları ve öznitelik değerlerini kategorilere atayabilirsiniz. Daha sonra çevrimiçi bir mağazaya kategori hiyerarşisi atarsınız.                            | [Perakende hiyerarşisi ayarlama](https://technet.microsoft.com/library/hh580593.aspx)</br> (AX için TechNet içeriği 2012)</br> [Öznitelikleri ve öznitelik türlerini ayarlama](https://technet.microsoft.com/library/hh227548.aspx) (AX için TechNet içeriği 2012)</br> [Perakende öznitelik grupları ayarlama](https://technet.microsoft.com/library/jj728713.aspx) (AX için TechNet içeriği 2012) |
| Çevrimiçi mağazayı kuruluş hiyerarşisine ekleyin. | Oluşturmuş olduğunuz çevrimiçi mağazaya ürün sınıflarını atayabilmeden veya siparişleri yerine getirebilmeden veya bu çevrimiçi mağazadan bilgileri içeren raporlar oluşturabilmeden önce, mağazayı bir ya da birden fazla kuruluş hiyerarşisine atamanız gerekir. En azından, çevrimiçi mağazayı ürün sınıfları içeren bir kuruluş hiyerarşisine atamanız gerekir. | [Bir çevrimiçi mağaza kurmak](https://technet.microsoft.com/library/jj682095.aspx) (AX 2012 için TechNet içeriği)                                                                                                                                                                                                                                                                                                     |
| Çevrimiçi mağazaya teslimat şekli ekle.          | Çevrimiçi mağazanın sunduğu teslimat yöntemlerini seçin.                                                                                                                                                                                                                                                                                                 | [Bir çevrimiçi mağaza kurmak](https://technet.microsoft.com/library/jj682095.aspx) (Microsoft AX 2012 için TechNet içeriği)                                                                                                                                                                                                                                                                                                     |
| Öznitelikleri eşle ve meta veri ekle.                   | Her kategori veya kanal ürününün Microsoft SharePoint sitesi çevrimiçi mağazasındaki özniteliklerin nasıl davranacağını belirten seçenekleri işaretleyin.                                                                                                                                                                                              | [Bir çevrimiçi mağaza kurmak](https://technet.microsoft.com/library/jj682095.aspx) (AX 2012 için TechNet içeriği)                                                                                                                                                                                                                                                                                                     |

## <a name="configure-online-store-products"></a>Çevrimiçi mağaza ürünlerini yapılandır

| Görev                                 | Ayrıntılı                                                                                                                                           | Konular                                                                                                                                                                                                                                                                            |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Çevrimiçi mağazaya ürün çeşidi ekle. | Bir çevrimiçi mağazada sunduğunuz ürünleri içeren sınıfları ekleyin.                                                                  | [Bir çevrimiçi mağaza kurmak](https://technet.microsoft.com/library/jj682095.aspx) (AX 2012 için TechNet içeriği)                                                                                                                                              |
| Katalogları yönet.                     | Mağazalarınızda sunmak istediğiniz ürünleri belirlemek için ürün kataloglarını kullanın.                                                              | [Anahtar görevler: Perakende ürün katalogları oluşturmak](https://technet.microsoft.com/library/jj728712.aspx) (AX 2012 için TechNet içeriği)                                                                                                                           |
| Fiyatları yönetin.                       | Fiyatlar ve indirimler, kanallar, kataloglar, bağlantılar ve bağlılık programları arasında merkezi bağlantı olan fiyat gruplarını ayarlayın ve kullanın. | [Fiyat gruplarını kullanarak fiyatları ayarlama](https://technet.microsoft.com/library/hh597169.aspx) (AX için TechNet içeriği 2012)</br> [Vergileri ayarlama](https://technet.microsoft.com/library/hh580571.aspx) (AX için TechNet içeriği 2012) |
| İskontoları yönetmek.                    | Dört tür indirim ve fiyat ayarlamalarını ayarlamak ve yönetmek.                                                                                  | [Fiyat ayarlamalarını ve iskontoları kurmak ve korumak](https://technet.microsoft.com/library/hh597114.aspx) (AX 2012 için TechNet içeriği)                                                                                                                          |
| Sevkiyat masraflarını yönetmek.             | Çevrimiçi mağazaya özel kargo ücretlerini ayarlayın ve yönetin.                                                                     | [Çevrimiçi mağazalar için kargo masraflarını ayarlamak](https://technet.microsoft.com/library/jj728714.aspx) (AX 2012 için TechNet içeriği)                                                                                                                           |
| Teslimat şekillerini yönet.            | Çevrimiçi mağazanın sunduğu teslimat modlarını yönetin.                                                                                        | [Teslimat modlarını ayarlamak](https://technet.microsoft.com/library/jj728719.aspx) (AX 2012 için TechNet içeriği)                                                                                                                                            |

## <a name="set-up-data-exchange-between-commerce-and-the-online-store"></a>Commerce ve çevrimiçi mağaza arasındaki veri değişimini ayarlama

| Görev                                 | Ayrıntılı                                                                                                                               | Konular                                                                                                                                                                                                                                                                                  |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kanal tümleştirme profillerini ayarlayın. | Profiller, bileşenlerin birbirleriyle iletişim kurabilmesini sağlar. Veri değişimi ayarlarını yapılandırmadan önce profiller ayarlayın. | [Gerçek zamanlı hizmet profili ayarlama](https://technet.microsoft.com/library/hh580631.aspx) (AX için TechNet içeriği 2012)</br> [Kanal profili ayarlama](https://technet.microsoft.com/library/jj677402.aspx) (AX için TechNet içeriği 2012) |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
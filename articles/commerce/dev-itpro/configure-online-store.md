---
title: Çevrimiçi mağazaları konfigüre et
description: Bu makale, bir çevrimiçi mağazayı merkezi olarak yapılandırma ve yönetme hakkında yardımcı olacak konulara bağlantılar sağlar.
author: kfend
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: 31541
ms.assetid: 7a25f9b4-a0bb-4e8c-95c0-c0799ec0620d
ms.search.region: Global
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 1acfe04b7e566ce8b3e3b5570be399621fbea974
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2021
ms.locfileid: "5937132"
---
# <a name="configure-online-stores"></a>Çevrimiçi mağazaları konfigüre et

[!include [banner](../includes/banner.md)]

Bu makale, bir çevrimiçi mağazayı merkezi olarak yapılandırma ve yönetme hakkında yardımcı olacak konulara bağlantılar sağlar.

Aşağıdaki tabloda listelenen konular, Commerce bileşenlerini ve istemcideki çevrimiçi mağazayı yapılandırmanıza yardımcı olur.

## <a name="configure-an-online-store"></a>Bir çevrimiçi mağazayı yapılandırma

| Görev                                                | Ayrıntılı                                                                                                                                                                                                                                                                                                                                                   | Konular                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bileşenleri yapılandırın.                        | Commerce operasyonları için bilgileri ayarlayın ve saklayın. Bu bilgiler, mağazalar, vergiler, ürünler, hediye kartları, promosyonlar ve indirimleri içerir.                                                                                                                                                                                                          | [Perakende'yi kurmak ve korumak](/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-retail) (Microsoft Dynamics AX 2012 için TechNet içeriği)                                                                                                                                                                                                                                                                                          |
| Bir kanal gezinme hiyerarşisi yapılandırın.    | Çevrimiçi bir mağazayla sunduğunuz ürünler için bir kategori yapısı ayarlamak için kanal gezinti kategori hiyerarşisi oluşturun. Kategori hiyerarşisini tanımlar ve ürünler, ürün öznitelik grupları ve öznitelik değerlerini kategorilere atayabilirsiniz. Daha sonra çevrimiçi bir mağazaya kategori hiyerarşisi atarsınız.                            | [Perakende hiyerarşisi ayarlama](/dynamicsax-2012/appuser-itpro/set-up-a-retail-hierarchy)</br> (AX için TechNet içeriği 2012)</br> [Öznitelikleri ve öznitelik türlerini ayarlama](/dynamicsax-2012/appuser-itpro/set-up-attributes-and-attribute-types) (AX için TechNet içeriği 2012)</br> [Perakende öznitelik grupları ayarlama](/dynamicsax-2012/appuser-itpro/set-up-retail-attribute-groups) (AX için TechNet içeriği 2012) |
| Çevrimiçi mağazayı kuruluş hiyerarşisine ekleyin. | Oluşturmuş olduğunuz çevrimiçi mağazaya ürün sınıflarını atayabilmeden veya siparişleri yerine getirebilmeden veya bu çevrimiçi mağazadan bilgileri içeren raporlar oluşturabilmeden önce, mağazayı bir ya da birden fazla kuruluş hiyerarşisine atamanız gerekir. En azından, çevrimiçi mağazayı ürün sınıfları içeren bir kuruluş hiyerarşisine atamanız gerekir. | [Bir çevrimiçi mağaza kurmak](/dynamicsax-2012/appuser-itpro/set-up-an-online-store) (AX 2012 için TechNet içeriği)                                                                                                                                                                                                                                                                                                     |
| Çevrimiçi mağazaya teslimat şekli ekle.          | Çevrimiçi mağazanın sunduğu teslimat yöntemlerini seçin.                                                                                                                                                                                                                                                                                                 | [Bir çevrimiçi mağaza kurmak](/dynamicsax-2012/appuser-itpro/set-up-an-online-store) (Microsoft AX 2012 için TechNet içeriği)                                                                                                                                                                                                                                                                                                     |
| Öznitelikleri eşle ve meta veri ekle.                   | Her kategori veya kanal ürününün Microsoft SharePoint sitesi çevrimiçi mağazasındaki özniteliklerin nasıl davranacağını belirten seçenekleri işaretleyin.                                                                                                                                                                                              | [Bir çevrimiçi mağaza kurmak](/dynamicsax-2012/appuser-itpro/set-up-an-online-store) (AX 2012 için TechNet içeriği)                                                                                                                                                                                                                                                                                                     |

## <a name="configure-online-store-products"></a>Çevrimiçi mağaza ürünlerini yapılandır

| Görev                                 | Ayrıntılı                                                                                                                                           | Konular                                                                                                                                                                                                                                                                            |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Çevrimiçi mağazaya ürün çeşidi ekle. | Bir çevrimiçi mağazada sunduğunuz ürünleri içeren sınıfları ekleyin.                                                                  | [Bir çevrimiçi mağaza kurmak](/dynamicsax-2012/appuser-itpro/set-up-an-online-store) (AX 2012 için TechNet içeriği)                                                                                                                                              |
| Katalogları yönet.                     | Mağazalarınızda sunmak istediğiniz ürünleri belirlemek için ürün kataloglarını kullanın.                                                              | [Anahtar görevler: Perakende ürün katalogları oluşturmak](/dynamicsax-2012/appuser-itpro/key-tasks-create-retail-product-catalogs) (AX 2012 için TechNet içeriği)                                                                                                                           |
| Fiyatları yönetin.                       | Fiyatlar ve indirimler, kanallar, kataloglar, bağlantılar ve bağlılık programları arasında merkezi bağlantı olan fiyat gruplarını ayarlayın ve kullanın. | [Fiyat gruplarını kullanarak fiyatları ayarlama](/dynamicsax-2012/appuser-itpro/setting-up-prices-using-price-groups) (AX için TechNet içeriği 2012)</br> [Vergileri ayarlama](/dynamicsax-2012/appuser-itpro/setting-up-taxes) (AX için TechNet içeriği 2012) |
| İskontoları yönetmek.                    | Dört tür indirim ve fiyat ayarlamalarını ayarlamak ve yönetmek.                                                                                  | [Fiyat ayarlamalarını ve iskontoları kurmak ve korumak](/dynamicsax-2012/appuser-itpro/setting-up-price-adjustments-and-discounts) (AX 2012 için TechNet içeriği)                                                                                                                          |
| Sevkiyat masraflarını yönetmek.             | Çevrimiçi mağazaya özel kargo ücretlerini ayarlayın ve yönetin.                                                                     | [Çevrimiçi mağazalar için kargo masraflarını ayarlamak](/dynamicsax-2012/appuser-itpro/set-up-shipping-charges-for-online-stores) (AX 2012 için TechNet içeriği)                                                                                                                           |
| Teslimat şekillerini yönet.            | Çevrimiçi mağazanın sunduğu teslimat modlarını yönetin.                                                                                        | [Teslimat modlarını ayarlamak](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery) (AX 2012 için TechNet içeriği)                                                                                                                                            |

## <a name="set-up-data-exchange-between-commerce-and-the-online-store"></a>Commerce ve çevrimiçi mağaza arasındaki veri değişimini ayarlama

| Görev                                 | Ayrıntılı                                                                                                                               | Konular                                                                                                                                                                                                                                                                                  |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kanal tümleştirme profillerini ayarlayın. | Profiller, bileşenlerin birbirleriyle iletişim kurabilmesini sağlar. Veri değişimi ayarlarını yapılandırmadan önce profiller ayarlayın. | [Gerçek zamanlı hizmet profili ayarlama](/dynamicsax-2012/appuser-itpro/set-up-a-real-time-service-profile) (AX için TechNet içeriği 2012)</br> [Kanal profili ayarlama](/dynamicsax-2012/appuser-itpro/set-up-a-channel-profile) (AX için TechNet içeriği 2012) |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
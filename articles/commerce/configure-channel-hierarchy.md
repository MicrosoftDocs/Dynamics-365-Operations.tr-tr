---
title: Bir kanalı kanal gezinme hiyerarşisini kullanacak şekilde yapılandırma
description: Bu konu, Microsoft Dynamics 365 Commerce'te bir kanal gezinme hiyerarşisi kullanmak üzere bir kanalın nasıl yapılandırılacağını açıklamaktadır.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 7b5041d35d310125c314ab2cb77d3cc40cdb7113
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416330"
---
# <a name="configure-a-channel-to-use-a-channel-navigation-hierarchy"></a>Bir kanalı kanal gezinme hiyerarşisini kullanacak şekilde yapılandırma


[!include [banner](includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce'te bir kanal gezinme hiyerarşisi kullanmak üzere bir kanalın nasıl yapılandırılacağını açıklamaktadır.

## <a name="overview"></a>Genel Bakış

Kanal gezinme hiyerarşileri, ürünleri kategoriler halinde düzenleyerek ürünlere bir e-ticaret sitesinde veya satış noktasında (POS) göz atılabilmesini sağlanır. Perakende ve çevrimiçi kanallar kanal gezinme hiyerarşileriyle yapılandırılmalıdır.

## <a name="configure-the-channel"></a>Kanalı yapılandırma

Kanal gezinme hiyerarşisini kullanacak şekilde kanalı yapılandırmak için bu adımları izleyin.

1. Gezinti bölmesinde, **Modüller \> Retail and commerce \> Kanal kurulumu \> Kanal kategorileri ve ürün öznitelikleri**'ne gidin.
1. Yapılandırılacak kanalı seçin.
1. Eylem bölmesinde, **Öznitelik meta verileri ayarla**'yı seçin.
1. **Kategori hiyerarşisi** açılır listesinde, uygun kanal gezinme hiyerarşisini seçin.
1. Eylem bölmesinde, **Kaydet**'i seçin.
1. **Öznitelik grubu** altında, tüm düğümler için genel öznitelikler olacak olan öznitelik gruplarını ekleyin.

Aşağıdaki resimde, bir kanalın kanal gezinme hiyerarşisini kullanacak şekilde nasıl yapılandırıldığı gösteriliyor.

![Örnek kanalı yapılandırması](media/configure-channel-hierarchy-1.png)

## <a name="set-attribute-metadata"></a>Öznitelik meta verileri ayarla

Öznitelik meta verilerinin ayarlanması, her bir düğümdeki özniteliklerin yapılandırılmasına izin verir.

Öznitelik meta verilerini ayarlamak için bu adımları izleyin.

1. Eylem bölmesinde, **Öznitelik meta verileri ayarla**'yı seçin.
1. Her bir düğüm için **Kanal ürün öznitelikleri**'ni seçin.
1. Kanalda düzelticileri etkinleştirmek için **Özniteliği kanalda göster** ayarını **Evet** ve **İyileştirilebilir** ayarını **Evet** yapın.
1. **Eylem bölmesinde** her düğümü istenildiği gibi yapılandırdıktan sonra, kaydetmek için **Kaydet** düğmesini seçin.
1. Bu ekrandan çıkıp **Kanal kategorileri ve ürün öznitelikleri** sayfasına dönmek için sağ üst köşedeki **X**'i seçin.

Aşağıdaki resimde, bir kanal kategori düğümünde yapılandırılmış kanal ürün öznitelikleri kümesi gösteriliyor.

![Kanal kategori düğümündeki kanal öznitelikleri](media/configure-channel-hierarchy-2.png)

## <a name="publish-changes"></a>Değişiklikleri yayımlama

Değişikliklerin yürürlüğe girmesi için, değişiklikleri yayımlamanız gerekir.

Değişiklikleri yayımlamak için bu adımları izleyin.

1. Eylem bölmesinde, **Kanal güncelleştirmelerini yayınla**'yı seçin.
1. **Kanal güncelleştirmelerini yayınla** bölmesinde **Tamam**'ı seçin.

Aşağıdaki resimde, kanal güncelleştirmelerinin nasıl yayımlanacağı gösteriliyor.

![Kanal güncelleştirmelerini yayınla](media/configure-channel-hierarchy-3.png)

## <a name="additional-resources"></a>Ek kaynaklar

[Kanal gezinme hiyerarşisi oluşturma](create-channel-hierarchy.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]
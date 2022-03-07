---
title: Bir kanalı kanal gezinme hiyerarşisini kullanacak şekilde yapılandırma
description: Bu konu, Microsoft Dynamics 365 Commerce'te bir kanal gezinme hiyerarşisi kullanmak üzere bir kanalın nasıl yapılandırılacağını açıklamaktadır.
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
ms.openlocfilehash: 3cf29bd423a2475b77e9076024b4da6864a31065da81de49f1b9a0f639243f1d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714004"
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

![Örnek kanal yapılandırması.](media/configure-channel-hierarchy-1.png)

## <a name="set-attribute-metadata"></a>Öznitelik meta verileri ayarla

Öznitelik meta verilerinin ayarlanması, her bir düğümdeki özniteliklerin yapılandırılmasına izin verir.

Öznitelik meta verilerini ayarlamak için bu adımları izleyin.

1. Eylem bölmesinde, **Öznitelik meta verileri ayarla**'yı seçin.
1. Her bir düğüm için **Kanal ürün öznitelikleri**'ni seçin.
1. Kanalda düzelticileri etkinleştirmek için **Özniteliği kanalda göster** ayarını **Evet** ve **İyileştirilebilir** ayarını **Evet** yapın.
1. **Eylem bölmesinde** her düğümü istenildiği gibi yapılandırdıktan sonra, kaydetmek için **Kaydet** düğmesini seçin.
1. Bu ekrandan çıkıp **Kanal kategorileri ve ürün öznitelikleri** sayfasına dönmek için sağ üst köşedeki **X**'i seçin.

Aşağıdaki resimde, bir kanal kategori düğümünde yapılandırılmış kanal ürün öznitelikleri kümesi gösteriliyor.

![Kanal kategori düğümündeki kanal öznitelikleri.](media/configure-channel-hierarchy-2.png)

## <a name="publish-changes"></a>Değişiklikleri yayımla

Değişikliklerin yürürlüğe girmesi için, değişiklikleri yayımlamanız gerekir.

Değişiklikleri yayımlamak için bu adımları izleyin.

1. Eylem bölmesinde, **Kanal güncelleştirmelerini yayınla**'yı seçin.
1. **Kanal güncelleştirmelerini yayınla** bölmesinde **Tamam**'ı seçin.

Aşağıdaki resimde, kanal güncelleştirmelerinin nasıl yayımlanacağı gösteriliyor.

![Kanal güncelleştirmelerini yayınlama.](media/configure-channel-hierarchy-3.png)

## <a name="additional-resources"></a>Ek kaynaklar

[Kanal gezinme hiyerarşisi oluşturma](create-channel-hierarchy.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]
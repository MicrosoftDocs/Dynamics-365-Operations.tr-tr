---
title: Çağrı merkezi kanalı ayarlama
description: Bu konuda, Microsoft Dynamics 365 Commerce'te yeni bir çağrı merkezi kanalının nasıl oluşturulacağı açıklanmaktadır.
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
ms.openlocfilehash: 42448bd54c00b8642b158f422e17d2b46ee25579
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057891"
---
# <a name="set-up-a-call-center-channel"></a>Çağrı merkezi kanalı ayarlama


[!include [banner](includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce'te yeni bir çağrı merkezi kanalının nasıl oluşturulacağı açıklanmaktadır.

## <a name="overview"></a>Genel Bakış

Dynamics 365 Commerce'te çağrı merkezi, uygulamada tanımlanabilen bir kanal türüdür. Çağrı merkezi varlıklarınız için bir kanal tanımlamak, sistemin belirli verileri ve sipariş işleme varsayılanlarını satış siparişlerine bağlamasına olanak sağlar. Bir şirket, Commerce'te birden fazla çağrı merkezi kanalı tanımlayabilir. 

Yeni bir çağrı merkezi kanalı oluşturmadan önce [Kanal kurulumu önkoşullarını](channels-prerequisites.md) tamamladığınızdan emin olun.

## <a name="create-and-configure-a-new-call-center-channel"></a>Yeni bir çağrı merkezi kanalı oluşturma ve yapılandırma

Yeni bir çağrı merkez kanalı oluşturmak ve yapılandırmak için bu adımları izleyin.

1. Gezinti bölmesinde **Modüller \> Kanallar \> Çağrı merkezleri \> Tüm çağrı merkezleri**'ne gidin.
1. Eylem bölmesinde **Yeni**'yi seçin.
1. **Ad** alanına yeni kanal için bir ad girin.
1. Açılır listeden uygun **Tüzel kişiliği** seçin.
1. Açılır listeden uygun **Ambar** yerleşimini seçin.
1. **Varsayılan müşteri** alanında, geçerli bir varsayılan müşteri girin.
1. **E-posta bildirimi profili** alanında, geçerli bir e-posta bildirimi profili girin.
1. Bir **Fiyat geçersiz kılma** bilgi kodu belirtin. Bunun için önce bir bilgi kodu oluşturmanız gerekebileceğini unutmayın.
1. Bir **Tutma kodu** bilgi kodu belirtin. Bunun için önce bir bilgi kodu oluşturmanız gerekebileceğini unutmayın.
1. Bir **Kredi** bilgi kodu belirtin. Bunun için önce bir bilgi kodu oluşturmanız gerekebileceğini unutmayın.
1. **Kaydet**'i seçin.

Aşağıdaki resimde yeni bir çağrı merkezi kanalının oluşturulması gösteriliyor.

![Yeni çağrı merkezi kanalı](media/channel-setup-callcenter-1.png)

Aşağıdaki resimde örnek bir çağrı merkezi kanalı gösteriliyor.

![Örnek çağrı merkezi kanalı](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a>Ek kanal ayarları

Çağrı merkezi kanalı kurulumu için gereken ek görevler ödeme yöntemlerini ve teslimat şekillerini ayarlamayı içerir.

Aşağıdaki resimde, **Ayarla** sekmesindeki **Teslimat şekilleri** ve **Ödeme yöntemleri** ayarlama seçenekleri gösteriliyor.

![Ek çağrı merkezi kanal kurulumu eylemleri](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a>Ödeme yöntemlerini ayarlama

Ödeme yöntemlerini ayarlamak için, bu kanalda desteklenen her ödeme türü için bu adımları izleyin.

1. Eylem bölmesinde, **Ayarla** sekmesini ve ardından **Ödeme yöntemleri**'ni seçin.
1. Eylem bölmesinde **Yeni**'yi seçin.
1. Gezinti bölmesinde, istediğiniz bir ödeme yöntemini seçin.
1. **Genel** bölümünde bir **İşlem adı** belirtin ve istediğiniz diğer ayarları yapılandırın.
1. Ödeme türü için gereken ek ayarları yapılandırın.
1. Eylem bölmesinde, **Kaydet**'i seçin.

Aşağıdaki resimde bir nakit ödeme yöntemi örneği gösteriliyor.

![Örnek ödeme yöntemleri](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a>Teslimat şekillerini ayarla

Yapılandırılan teslimat şekillerini, **Eylem bölmesindeki** **Ayarla** sekmesinden **Teslimat şekilleri**'ni seçerek görebilirsiniz.  

Bir teslimat şekli eklemek veya değiştirmek için bu adımları izleyin.

1. Gezinti bölmesinde **Modüller \> Stok yönetimi \> Teslimat şekilleri**'ne gidin.
1. Eylem bölmesinde, yeni bir teslimat şekli oluşturmak için **Yeni**'yi seçin veya varolan bir şekli seçin.
1. **Perakende kanalları** bölümünde, kanalı eklemek için **Satır ekle**'yi seçin. Kanalları tek tek eklemek yerine kuruluş düğümleri kullanarak eklemek, kanal eklemeyi kolaylaştırabilir.

Aşağıdaki resimde bir teslimat şekli örneği gösteriliyor.

![Teslimat şekillerini ayarla](media/channel-setup-retail-7.png)

## <a name="additional-resources"></a>Ek kaynaklar

[Kanal kurulum önkoşulları](channels-prerequisites.md)

[Çağrı merkezi satış işlevi](call-center-functionality.md)

[Çağrı merkezi sipariş işleme seçeneklerini ayarlama](set-up-order-processing-options.md)

[Çağrı merkezi katalogları](call-center-catalogs.md)

[Sahtekarlık uyarılarını ayarlama ve bunlarla çalışma](set-up-fraud-alerts.md)

[Çağrı merkezleri için süreklilik programları ayarlama](set-up-continuity-program.md)

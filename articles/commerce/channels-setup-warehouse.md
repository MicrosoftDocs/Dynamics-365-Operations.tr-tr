---
title: Ambar ayarlama
description: Bu konuda, Microsoft Dynamics 365 Commerce'te yeni bir kanalla kullanılacak bir ambarın nasıl ayarlanacağı açıklanmaktadır.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 67c0bb169bee8a7ea90edb4db7233111a8ee6e34
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993665"
---
# <a name="warehouse-set-up"></a>Ambarı ayarlama


[!include [banner](includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce'te yeni bir kanalla kullanılacak bir ambarın nasıl ayarlanacağı açıklanmaktadır.

## <a name="overview"></a>Genel Bakış

Her Commerce kanalı, yapılandırılmış bir ambarın kendisiyle ilişkilendirilmesini gerektirir. Aşağıdaki yordamlarda, bir Commerce kanalı için ambar ayarlamak üzere gereken minimum yapılandırma verilmektedir. Ambar kurulumuyla ilgili daha fazla bilgi için lütfen [Ambar yönetimine genel bakış](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json)'a bakın.

## <a name="configure-a-warehouse-site"></a>Bir ambar tesisini yapılandırma

Ambarı ayarlamadan önce bir ambar tesisi yapılandırmanız gerekir.

Bir ambar tesisini yapılandırmak için bu adımları izleyin.

1. Gezinti bölmesinde **Modüller \> Perakende ve ticaret \> Kanal kurulumu \> Tesisler**'e gidin.
1. Eylem bölmesinde **Yeni**'yi seçin.
1. **Tesis** alanına bir değer girin.
1. **Ad** alanına bir değer girin.
1. **Genel** bölümünde, uygun **Saat dilimini** ayarlayın.
1. **Adresler** bölümünde bir adres girin.
1. Eylem bölmesinde, **Kaydet**'i seçin.

Aşağıdaki resimde örnek bir ambar tesisi gösterilmektedir.

![Örnek ambar tesisi](media/warehouse-site.png)

## <a name="set-up-a-warehouse"></a>Ambar ayarlama

Bir ambarı ayarlamak için bu adımları izleyin.

1. Gezinti bölmesinde **Modüller \> Perakende ve ticaret \> Kanal kurulumu \> Ambarlar**'a gidin.
1. Eylem bölmesinde **Yeni**'yi seçin.
1. **Ambar** alanına bir değer girin.  Bu, bir mağazayla 1:1 eşleşme ise mağaza adını veya bir bölgesel dağıtım merkezinin adını kullanmayı düşünebilirsiniz.
1. **Ad** alanına bir değer girin.
1. **Tesis** açılır listesinde, önceden oluşturulan ambar tesisini seçin.
1. **Tür** alanında, **Varsayılan**'ı seçin.
    - Bir **Karantina ambarı** ayarlamak istiyorsanız, bu adımları izleyerek, **Tür** ayarı **Karantina** olan ek bir ambar oluşturmanız gerekir.
    - Bir **Transit ambarı** ayarlamak istiyorsanız, bu adımları izleyerek, **Tür** ayarı **Transit** olan ek bir ambar oluşturmanız gerekir.
1. Eylem bölmesinde, **Kaydet**'i seçin.

## <a name="set-up-inventory-aisles"></a>Stok koridorlarını ayarla

Stok koridorları ayarlamak için bu adımları izleyin.

1. Gezinti bölmesinde **Modüller \> Perakende ve ticaret \> Kanal kurulumu \> Yerleşim ayarı \> Stok koridorları**'na gidin.
1. Eylem bölmesinde **Yeni**'yi seçin.
1. **Ambar** açılır listesinde, önceden oluşturulan ambarı seçin.
1. **Koridor** alanına bir ad girin (örneğin "Var").
1. **Ad** alanına bir ad girin (örneğin "Varsayılan koridor").
1. Eylem bölmesinde, **Kaydet**'i seçin.

## <a name="set-up-warehouse-inventory-locations"></a>Ambar stok yerleşimlerini ayarlama

Standart, hasarlı ve iade stok için ambar stok yerleşimleri ayarlamak üzere bu adımları izleyin.

1. Gezinti bölmesinde **Modüller \> Perakende ve ticaret \> Kanal kurulumu \> Ambarlar**'a gidin.
1. Daha önce oluşturduğunuz ambarı seçin.
1. Eylem bölmesinde, **Düzenle**'yi seçin.
1. Eylem bölmesinde **Ambar**'ı ve ardından **Stok yerleşimi**'ni seçin.
1. Eylem bölmesinde **Yeni**'yi seçin. **Ambar** açılır listesi varsayılan olarak yeni ambarınızı gösterecektir.
    1. **Koridor** kutusuna, daha önce belirttiğiniz koridorun adını girin. 
    1. **El ile güncelleştirme** ayarını **Evet** yapın.
    1. **Yerleşim** kutusuna ambarın adını girin.
    1. Eylem bölmesinde, **Kaydet**'i seçin.
 1. Eylem bölmesinde **Yeni**'yi seçin.  **Ambar** açılır listesi varsayılan olarak yeni ambarınızı gösterecektir.
    1. **Koridor** kutusuna, daha önce belirttiğiniz koridorun adını girin.  
    1. **El ile güncelleştirme** ayarını **Evet** yapın.
    1. **Yerleşim** kutusuna "Hasarlı" girin.
    1. Eylem bölmesinde, **Kaydet**'i seçin.
 1. Eylem bölmesinde **Yeni**'yi seçin.  **Ambar** açılır listesi varsayılan olarak yeni ambarınızı gösterecektir.
    1. **Koridor** kutusuna, daha önce belirttiğiniz koridorun adını girin. 
    1. **El ile güncelleştirme** ayarını **Evet** yapın.
    1. **Yerleşim** kutusuna "İadeler" girin.
    1. Eylem bölmesinde, **Kaydet**'i seçin.
    
Aşağıdaki resimde San Francisco'daki bir ambar stok yerleşiminin kurulumu gösterilmektedir.

![Örnek stok yerleşimi kurulumu](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a>Ambar kurulumunu tamamlama

Ambar kurulumunu tamamlamak için bu adımları izleyin.

1. Gezinti bölmesinde **Modüller \> Perakende ve ticaret \> Kanal kurulumu \> Ambarlar**'a gidin.
1. Daha önce oluşturduğunuz ambarı seçin.
1. Eylem bölmesinde, **Düzenle**'yi seçin.
1. **Stok ve ambar yönetimi** altında:
    1. **Varsayılan yerleşim konumu**'nu yukarıda oluşturulan varsayılan yerleşime ayarlayın.
    1. **Varsayılan çıkış yeri yerleşimi**'ni yukarıda oluşturulan varsayılan yerleşime ayarlayın.
1. **Adresler** bölümü altında bir ambar adresi girin.
1. **Perakende** bölümünün altında: 
    1. **Varsayılan iade yerleşimi** kutusuna, önceden oluşturulan iade yerleşimini girin.
    1. **Mağaza**'yı **Evet** olarak ayarlayın.
    1. **Ağırlık** ayarını **1,00** yapın. 
    1. **Depolama Boyutları** kutusuna, önceden oluşturulan varsayılan yerleşimi girin.
1. **Ambar** bölümünün altında, **Fiziksel negatif stok** ayarını **Evet** yapın.
1. Eylem bölmesinde, **Kaydet**'i seçin.

Aşağıdaki resimde, yapılandırılmış bir ambarın ayrıntıları gösterilmektedir.

![Yapılandırılmış ambar örneği](media/warehouse-sample.png)

## <a name="additional-resources"></a>Ek kaynaklar

[Ambar yönetimine genel bakış](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json)

[Kanallara genel bakış](channels-overview.md)

[Kanal kurulum önkoşulları](channels-prerequisites.md)

[Perakende kanalını ayarlama](channel-setup-retail.md)
    
[Çevrimiçi kanal ayarlama](channel-setup-online.md)

[Çağrı merkezi kanalını ayarlama](channel-setup-callcenter.md)






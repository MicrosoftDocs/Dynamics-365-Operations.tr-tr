---
title: Şablonları yükle
description: Bu makalede, yük şablonlarının nasıl ayarlanacağı ve yük şablonunun yeni bir yük ile nasıl ilişkilendirileceği açıklanmaktadır.
author: Weijiesa
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: weijiesa
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 47b4925c528b64b835ce3e88659ee6ab0572eb2b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8844195"
---
# <a name="load-templates"></a>Şablonları yükle

[!include [banner](../../includes/banner.md)]

Yeni bir yük oluştururken bir yük şablonu atayabilirsiniz. Yük şablonu, ekipmanlarla ve yükün yüksekliği, genişliği, derinliği ve hacmi gibi ölçülerle ilgili bilgileri içerir.

Bu makalede, yük şablonlarının nasıl ayarlanacağı ve yük şablonunun yeni bir yük ile nasıl ilişkilendirileceği açıklanmaktadır.

## <a name="set-up-a-load-template"></a>Yük şablonu ayarlama

1. **Taşıma yönetimi \> Kurulum \>Yük Oluşturma \> Yük şablonu**'na gidin.
1. Eylem bölmesinde, yeni şablon eklemek için **Yeni**'yi veya var olan bir şablonu düzenlemek için **Düzenle**'yi seçin.
1. Yeni veya var olan şablon satırında, aşağıdaki alanları ayarlayın:

    - **Yük şablonu kodu**: Yük şablonu için benzersiz bir tanımlayıcı (kod) girin.
    - **Ekipman**: Yükü sevk etmek için kullanılması gereken ekipmanı seçin.
    - **Yük yüksekliği**, **Yük genişliği** ve **Yük derinliği**: Yükün boyutlarını girin.
    - **İzin verilen maksimum yük hacmi** ve **İzin verilen maksimum yük ağırlığı**: İzin verilen maksimum yük hacmi ve yük ağırlığını girin.
    - **İzin verilen maksimum brüt ağırlık**: Yük için izin verilen maksimum brüt ağırlığını girin. Yükün brüt ağırlığına dara ağırlığı ve yük ağırlığı dahildir.
    - **İzin verilen maksimum navlun parçası sayısı**: Yükün içerebileceği maksimum navlun parçası sayısını girin.
    - **Yükü zemine yığ**: Zeminden yüklemeyi kullanmak için bu onay kutusunu işaretleyin. Bir kat yükleme senaryosunda, kapasiteyi maksimum düzeye çıkartmak için kutular konteyner içinde yerden tavana kadar ve duvardan duvara yığılır.

1. Eylem bölmesinde, **Kaydet**'i seçin.

## <a name="associate-a-load-template-with-a-new-load"></a>Yeni bir yük ile bir yük şablonunu ilişkilendirme

1. **Taşıma yönetimi \> Planlama \> Yük planlama çalışma ekranı**'na gidin.
1. Sayfanın üst kısmından, yük oluşturduğunuz kaynak belgenin türüne göre aşağıdaki sekmelerden birini seçin: **Sevkiyatlar**, **Satış satırları**, **Transfer satırları** veya **Satın alma siparişi satırları**. 
1. Yükü planlamak için belirli bir belge seçin.
1. Eylem Bölmesinde **Arz ve talep** sekmesindeki **Ekle** grubunda **Yeni yüke**'yi seçin.
1. **Yük şablonu** iletişim kutusunda **Yük şablonu kodu** alanından, uygulanacak şablonu seçin.
1. Şablonu uygulamak için **Tamam**'ı seçin.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
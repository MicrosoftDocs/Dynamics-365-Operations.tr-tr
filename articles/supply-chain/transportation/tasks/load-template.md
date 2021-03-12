---
title: Şablonları yükle
description: Bu konuda, yük şablonlarının nasıl ayarlanacağı ve yük şablonunun yeni bir yük ile nasıl ilişkilendirileceği açıklanmaktadır.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 0a4070a1dd5d53bb502ba2ab0c91dbdc90ded34d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005064"
---
# <a name="load-templates"></a>Şablonları yükle

Yeni bir yük oluştururken bir yük şablonu atayabilirsiniz. Yük şablonu, ekipmanlarla ve yükün yüksekliği, genişliği, derinliği ve hacmi gibi ölçülerle ilgili bilgileri içerir.

Bu konuda, yük şablonlarının nasıl ayarlanacağı ve yük şablonunun yeni bir yük ile nasıl ilişkilendirileceği açıklanmaktadır.

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

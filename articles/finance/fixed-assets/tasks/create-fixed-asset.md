---
title: Sabit kıymet oluşturma
description: Bu konu, sabit kıymet listesi sayfasından yeni bir sabit kıymet kaydının nasıl oluşturulacağını açıklamaktadır.
author: moaamer
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a9394c0c7a5e2d9b417cbaee9f4e67f36ae124fb
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/05/2022
ms.locfileid: "8714299"
---
# <a name="create-a-fixed-asset"></a>Sabit kıymet oluşturma

[!include [banner](../../includes/banner.md)]

Bu konu, **sabit kıymet** listesi sayfasından yeni bir sabit kıymet kaydının nasıl oluşturulacağını açıklamaktadır.

Sistem sabit kıymet grubuna atanan numara serisine göre kıymet numarasını atar. Microsoft Excel eklentisi aracılığıyla kıymetleri içe aktarmak için sabit kıymet şablonunu veya başka bir içe aktarma işini kullanırsanız sistem otomatik olarak sabit kıymet kayıtları oluşturur ve kıymet numarasını arttırır.

Bir kıymet kaydını el ile oluşturmak için aşağıdaki adımları izleyin.

1. **Gezinti bölmesi \> Modüller \> Sabit kıymetler \> Sabit kıymetler \> Sabit kıymetler**'e gidin.
2. **Eylem bölmesinde** **Yeni**'yi seçin.
3. **Sabit kıymet grubu** alanında bir değer girin veya seçin. **Sabit kıymet parametreleri**'nde ve **Sabit kıymet grubu**'nda **Sabit kıymetleri otomatik numaralandır** işlevini etkinleştirdiyseniz **Numara**'ya varsayılan değer atanır. Etkinleştirmediyseniz, sabit kıymeti tanımlayacak benzersiz bir numara girmeniz gerekir.
4. **Ad** alanına bir değer girin. İşletmenizin bu kıymet için gereksinim duyacağı ek bilgileri girin.
5. **Eylem Bölmesi**'nde, **Defterler**'i seçin.
6. **Alım tarihi** alanına bir tarih girin.
7. **Alım fiyatı** alanına bir sayı girin.

    - İşletmenizin bu defter için gereksinim duyacağı ek bilgileri girin.
    - İşletmenizin kalan defterler için gereksinim duyacağı ek bilgileri girin.

8. Sayfayı kapatın.

Ayrıca, Excel eklentisini kullanarak veya **veri yönetimi** çalışma alanından içe aktarma işi çalıştırarak da sabit kıymetleri içe aktarabilirsiniz. İçe aktarmayı çalıştırmadan önce, şablondaki gerekli alanların değerlerini girin.

Bir sabit kıymet numarasını Excel eklentisinin şablonunda veya veri yönetimi'nde tanımlamadıysanız, sistem her içe aktarılan kıymet için bir sabit kıymet numarası oluşturur ve her birinin numara serisini otomatik olarak arttırır. Ancak, varlıkları içe aktarır ve şablonda kıymet numaralarını tanımlarsanız, sistem numara serisini otomatik olarak **artırmaz**. Bu durumda bir yöneticinin numara serisini el ile güncelleştirmesi gerekebilir. Sabit kıymet numarasını Excel eklentisinin şablonunda tanımladıysanız, sistem tanımlanan sabit kıymet numarasını kullanır ve numara serisini arttırır.

> [!NOTE]                                                                                                         
> Amortismanı deftere naklettikten sonra **Hizmete giriş** ve **İlk amortisman göreceği tarih** alanları **Defter** sayfasında kilitli olur. Ayrıca her iki alan da veri varlığından güncelleştirilmez.

> [!WARNING]
> Hareketler ilişkili deftere nakledilirse veya yeni oluşturulan sabit varlık günlük satırına girilir ancak deftere nakledilmezse sabit varlık kaydı silinmez. 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

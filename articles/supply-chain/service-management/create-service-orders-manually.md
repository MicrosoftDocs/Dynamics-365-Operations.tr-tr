---
title: Servis siparişlerini el ile oluşturma
description: Servis siparişlerini, bir servis sözleşmesi kullanarak veya **Servis siparişleri** formunu kullanarak el ile oluşturabilirsiniz.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d80461694a28a0842155cbd8ca224c37bd85dde7
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3202710"
---
# <a name="create-service-orders-manually"></a>Servis siparişlerini el ile oluşturma    

[!include [banner](../includes/banner.md)]


Servis siparişlerini, bir servis sözleşmesi kullanarak veya **Servis siparişleri** formunu kullanarak el ile oluşturabilirsiniz. Aynı zamanda bir projeden servis siparişi oluşturabilirsiniz.

> [!TIP]
> <P>Servis siparişleri oluşturmak için otomatik işlemleri kullanabilirsiniz. 

## <a name="create-a-service-order-manually-from-a-service-agreement"></a>Servis sözleşmesinden el ile servis siparişi oluşturma

1.  **Servis yönetimi** \> **Ortak** \> **Servis sözleşmeleri** \> **Servis sözleşmeleri**'ne tıklayın.

2.  Bir servis anlaşması seçin veya yeni bir servis anlaşması oluşturun.

3.  **Teslim et** sekmesine tıklayın, **Oluştur** grubunda **Planlanan servis siparişleri**'ne tıklayarak **Servis siparişleri oluştur** formunu açın.

## <a name="create-a-service-order-manually-in-the-service-orders-form"></a>Servis siparişleri formunda el ile servis siparişi oluşturma

1.  **Servis yönetimi** \> **Ortak** \> **Servis siparişleri** \> **Servis siparişleri**'ne tıklayın.

2.  Yeni bir servis siparişi oluşturmak için Ctrl+N tuşlarına basın.

3.  Servis siparişi için servis siparişi satırları oluşturun.

> [!NOTE]
> <P><STRONG>Servis yönetimi parametreleri</STRONG> formundaki <STRONG>Servis sözleşmesi olmadan izin ver</STRONG> onay kutusu işaretlenirse servis siparişini servis sözleşmesine iliştirmeden servis siparişi satırlarından hareketleri nakledebilirsiniz. Onay kutusu işaretlenmezse, servis siparişi satırlarını nakletmeden önce projeye el ile oluşturulan servis siparişini iliştirmelisiniz.</P>

## <a name="create-a-service-order-from-a-project"></a>Projeden bir servis siparişi oluşturma

1.  **Proje yönetimi ve muhasebe** \> **Genel** \> **Projeler** \> **Tüm projeler**'e tıklayın.

2.  **Projeler** formunda, **Eylem bölmesinde** **Yönet** sekmesine tıklayın \> **Servis** \> **Servis siparişleri**'ne tıklayın.

3.  **Servis siparişleri** formunda önceki el ile servis siparişi oluşturma yordamını takip edin. **Proje kodu** alanı proje referansını gösterir.

> [!NOTE]
> <P><STRONG>Servis yönetimi parametreleri</STRONG> formundaki <STRONG>Servis sözleşmesi olmadan izin ver</STRONG> onay kutusu işaretlenirse servis siparişini servis sözleşmesine iliştirmeden servis siparişi satırlarından hareketleri nakledebilirsiniz. Onay kutusu işaretlenmezse, servis siparişi satırlarını nakletmeden önce projeye el ile oluşturulan servis siparişini iliştirmelisiniz.</P>

## <a name="create-a-service-order-from-the-sales-order-form"></a>Satış siparişi formundan servis siparişi oluşturma

**Satış siparişine dayalı yeni bir servis siparişi oluştur** sihirbazını kullanarak **satış siparişleri** formundan bir servis siparişi oluşturabilirsiniz.

1.  **Satış ve pazarlama** \> **Yaygın** \> **Satış siparişleri** \> **Tüm satış siparişleri**'ne tıklayın.

2.  İlgili satış siparişini açın.

3.  **Satış siparişi** sekmesinde, **Servis siparişi**'ne tıklayarak **Satış siparişine dayalı yeni bir servis siparişi oluştur** sihirbazını başlatın.

4.  **İleri \>** seçeneğine tıklayın, **Servis siparişi için sözleşme seç** sayfasında aşağıdaki adımları tamamlayın:
    
      - Yeni servis siparişinin ilişkilendirilmesi gereken servis sözleşmesini seçmek için **Servis sözleşmesi** alanını işaretleyin.
    
      - İsteğe bağlı: Bu servis siparişini belirli bir projeyle ilişkilendirmek için **Proje Kodu** alanını kullanın.

5.  **İleri \>** seçeneğine tıklayın, **Servis siparişi oluştur** sayfasında aşağıdaki adımları tamamlayın:
    
      - **Tercih edilen servis zamanı** alanında servis çağrısının başlayacağı tarih ve saati girin.
    
      - İsteğe bağlı: **Açıklama** alanındaki metni değiştirin. Varsayılan olarak bu alan önceki sayfada seçtiğiniz servis sözleşmesinin açıklamasını içerir.
    
      - **Sorumlu** alanında, sözleşmeden sorumlu olan çalışanın kimliğini ve ne olduğunu biliyorsanız, müşterinin servis çağrısı için tercih ettiği teknisyenin kimliğini girin.
    
      - **İlgili Kişi Kimliği** alanında müşterinin şirketinde bu servis siparişiyle ilgili olarak sizinle bağlantı kurması gereken kişiyi seçin.

6.  **İleri\>** seçeneğine ve **Bitir**'e tıklayın.


## <a name="see-also"></a>Ayrıca bkz.

[Servis emirleri](service-orders.md)

[Servis siparişlerini otomatik olarak oluşturma](create-service-orders-automatically.md)

[Servis siparişleri oluştur (sınıf formu)](https://technet.microsoft.com/library/aa553901\(v=ax.60\)) 

